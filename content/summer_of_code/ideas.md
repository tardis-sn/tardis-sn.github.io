---
title: "GSoC 2026 Ideas"
date: 2026-01-22
draft: false
layout: page
aliases:
    - /gsoc/ideas
---

## Table of Contents

1. [Astronomy and Astrophysics Background](#astronomy-and-astrophysics-background)
2. [The TARDIS Project](#the-tardis-project)
3. [List of GSoC 2026 Project Ideas](#list-of-gsoc-2026-project-ideas)
   - [Rewrite the Custom Abundance Widget in Panel](#rewrite-the-custom-abundance-widget-in-panel)
   - [TARDIS Setups Generated Plots and Gallery](#tardis-setups-generated-plots-and-gallery)
   - [Continuum Opacity Source Reader](#continuum-opacity-source-reader)
   - [Benchmark Optimisation](#benchmark-optimisation)
   - [Improving Test Coverage for Plasma Module](#improving-test-coverage-for-plasma-module)


### Astronomy and Astrophysics Background:

A <a href="https://en.wikipedia.org/wiki/Supernova" target="_blank">supernova</a>(here we show SN1994D in the Galaxy NGC4526 - image source: wikipedia) marks the brilliant death throes of a star, during which it outshines its entire galaxy. It not only marks death, though: supernova ejecta change the evolution of the universe and enable the formation of planets and life as we know it. From the iron in your blood to the silicon in your laptop, supernovae return heavy elements assembled from the primordial hydrogen and helium left after the big bang.

<img src="/images/480px-SN1994D.jpg" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">
There are still many mysteries surrounding supernovae (e.g. their precise origins, inner workings, …). One way to study these objects in more detail is to split the light coming from these objects into its components (like using a prism) and analyzing the resulting data (which is called a spectrum). Here, we show spectra (black lines) of a number of different supernova types (image courtesy Daniel Kasen and LBL). Different chemical elements present in the supernova leave their mark on the spectra by imprinting characteristic features, so-called atomic lines (regions highlighted in colour). Thus, studying and interpreting such spectra allows us to identify what supernovae are made of.

<img src="/images/sn_types.jpg" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

With sophisticated computer simulations astronomers try to reproduce the observed spectra to draw conclusion about the properties of the supernova ejecta and ultimately the explosion mechanism and progenitor stars. TARDIS is such a numerical code. It calculates theoretical spectra based on a number of input parameters, such as the supernova brightness and the abundances of the different chemical elements present in the ejecta (e.g. Oxygen, Silicon, Iron, etc.). The main idea for this procedure is that by finding a close match between theoretical and observed spectra we identify the parameters that actually describe the supernovae.

### The TARDIS Project

As mentioned in the background information above, TARDIS is a scientific tool (more specifically a Monte Carlo radiative transfer code) whose primary goal is the calculation of theoretical spectra for supernovae. Below, you find the typical result of a TARDIS calculation. It shows the calculated synthetic spectra for a simple supernova model. This particular setup (tardis_example) is officially provided by the TARDIS collaboration on the <a href="https://tardis-sn.github.io/tardis/" target="_blank">documentation</a>.
<img src="/images/tardis_example.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

### List of GSoC 2026 Project Ideas

In the TARDIS collaboration we first establish a detailed plan on implementing new features before starting the actual work. This is an important step that ensures that the entire TARDIS collaboration is informed about the development efforts and that the team members can help shape the ideas during the discussion phase. We call these documents TEP - TARDIS Enhancement Proposals. We already have a great list of ideas <a href="https://github.com/tardis-sn/tep" target="_blank">here</a> that we need help with. Some of these we have specially selected for GSoC 2026 and are listed with specific "warm-up" tasks below. But feel free to propose your own TEP and make a PR on that.

If you use one of our TEPs, you can definitely add more detail to the implementation, but what we really want to see is a detailed timeline with milestones that shows us that you have thought about how to implement the feature in three months. For any questions about the projects, please ask on <a href="https://gitter.im/tardis-sn/gsoc" target="_blank">Gitter</a>.

Putting in a <a href="https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request" target="_blank">Pull Request</a> with the First objective is essential for each proposal to allow to see how you work.

***NOTE:***
Please also read our [AI and LLM Usage Policy](../ai_usage_policy).

#### Rewrite the Custom Abundance Widget in Panel

<img src="/gsoc_2026/panel.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Hard \
**Mentors:** Andrew Fullard, Atharva Arya, James Gillanders, Jaladh Singhal \
**Description:** TARDIS has a collection of visualisation tools and widgets to interactively explore TARDIS simulations which run inside Jupyter Notebooks. A lot of these modules currently depend on dependencies like ipywidgets which do not work well with our Sphinx documentation. Some of these tools have already been migrated but we want to migrate the rest of our widgets to panel too. For this project, you will be working on migrating the custom abundance widget to Panel.

Visualisation Module:
https://tardis-sn.github.io/tardis/analyzing_tardis/visualization/index.html#tardis-widgets-graphical-user-interfaces

**First Objective:** The shell info widget is already migrated to panel but it is not fully interactive on the documentation. Make it work as it works in the notebooks. 
See <a href="https://tardis-sn.github.io/tardis/analyzing_tardis/visualization/how_to_generating_widgets.html#How-to-Generate-Data-Exploration-Widgets" target="_blank">documentation here</a>.

**Expected Outcomes:**
- The custom abundance widget moved to Panel.
- Visualisation tools and widgets can be embedded on the website allowing users to interact with them.
- Comprehensive documentation and tests for all code written.

#### TARDIS Setups Generated Plots and Gallery

<img src="/gsoc_2026/tardis-setups-gen-plots.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Medium \
**Mentors:** Josh Shields, Andrew Fullard \
**Description:** The TARDIS umbrella includes a repository for people to put models and simulations that have been used in scientific studies, found at <a href="https://github.com/tardis-sn/tardis-setups" target="_blank">tardis-setups</a>. However, there is very little ability for people to look at what is there, or glean information from the TARDIS models that would be produced by the inputs that live in the repository. This project proposes to develop a template notebook that would be run with every set of TARDIS inputs in the TARDIS setups repository. This notebook would provide a brief overview of the inputs used to generate TARDIS spectra, and an analysis visualization output generated with those TARDIS inputs. This would allow for a quick glimpse into which models exist in the repository, and could also serve as a jumping off point for people who want to create new models, since they will have access to a suite of verified working TARDIS inputs and simulations.

This project could be extended to include a web development component, where the notebook described in the last paragraph could be displayed for each set of inputs that exist in TARDIS setups, and could be easily browsed. This would also include either a pipeline for new submissions to the TARDIS setups repository to automatically produce new notebooks as well.

**First Objective:** Create a notebook that produces the various visualization tools that TARDIS simulations can produce. Validate that the notebook works with a variety of TARDIS inputs.

**Expected Outcomes:**
- Visualization notebook that demonstrates a run of TARDIS, as well as the various analysis tools TARDIS offers.
- A revamping of the TARDIS setups repository to accommodate generating the notebook with the models that exist in the TARDIS setups repository.
- An easy to use pipeline that runs for new submissions to the TARDIS setups repository.

#### Continuum Opacity Source Reader

<img src="/gsoc_2026/carsus3.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Hard \
**Mentors:** Andrew Fullard, Josh Shields \
**Description:** There's a lot of literature with useful tables for the TARDIS codebase and other scientific codes in pdfs (e.g. <a href="https://academic.oup.com/mnras/article/266/4/805/982644" target="_blank">this paper</a>), or often in dataproducts. <a href="https://tardis-sn.github.io/carsus/" target="_blank">Carsus</a> currently reads in data from standard sources and archives (<a href="https://www.chiantidatabase.org/" target="_blank">Chianti</a>, <a href="https://sites.pitt.edu/~hillier/web/CMFGEN.htm" target="_blank">CMFGEN</a>), but does not flexibly read data from sources in the literature. The goal of this project is to expand Carsus to read datatables like ones in this work, with potential expansion for a future-proof workflow (new opacity tables). These could all go in a new tardis repository called "carsus-literature-tables" or something along those lines. You can look at <a href="https://github.com/tardis-sn/carsus-data-molecules-barklem2016" target="_blank">carsus-data-molecules-barklem2016</a> for an example of preprocessed datatables ready to be ingested by Carsus.

**First Objective:** Read one of the datatables from <a href="https://cdsarc.cds.unistra.fr/viz-bin/cat/VI/80#/browse" target="_blank">this archive</a> (try s92.201.gz, under ftp) and process it into a pandas dataframe. Look to do this in a programmatic way that could be reused for similar files. See section 6.4 of <a href="https://articles.adsabs.harvard.edu/pdf/1994MNRAS.266..805S" target="_blank">this paper</a> for more details on table contents and formatting if desired.

**Expected Outcomes:**
- Code that reads in the new dataproducts and integrates with Carsus.
- Comprehensive documentation and tests for all code written.

#### Benchmark Optimisation

<img src="/gsoc_2026/benchmark.png" alt="image" style="display: block; margin: 0 auto;width: 75%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Hard \
**Mentors:** Andrew Fullard, Atharva Arya \
**Description:** TARDIS commits are monitored by a benchmarking framework to detect performance regressions. But the current framework only tests 5 commits at a time and not with much detail. The goal of this project is to improve the benchmarking framework by adding more benchmarks. This project will also add more benchmarks to STARDIS, a related code. The second stage of the project will use the benchmarks to investigate possible performance improvements to TARDIS and STARDIS.

<a href="https://tardis-sn.github.io/tardis-benchmarks/" target="_blank">TARDIS Benchmarks</a> | <a href="https://tardis-sn.github.io/stardis-benchmarks/" target="_blank">STARDIS Benchmarks</a>

**First Objective:** Benchmark the Plasma solver factory: <a href="https://github.com/tardis-sn/tardis/blob/master/tardis/plasma/assembly/base.py" target="_blank">base.py</a> and share the ASV results for the last 5 commits along with the code in a pull request.

**Expected Outcomes:**
- Exhaustive benchmarks that time important TARDIS modules like plasma, transport, visualisation to name a few.
- Larger history of benchmarks (currently only 5) and regenerating benchmarks for failed commits to avoid losing benchmark history.
- Comprehensive documentation and tests for all code written.

#### Improving Test Coverage for Plasma Module

<img src="/gsoc_2026/test_cov.png" alt="image" style="display: block; margin: 0 auto;width: 75%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Medium \
**Mentors:** Andrew Fullard, Atharva Arya, Josh Shields \
**Description:** TARDIS has an extensive tests suite, a significant part of which is not reflected in the coverage. The goal of this project is to find untested code for the plasma module specifically and improve its test coverage.

**First Objective:** Investigate the plasma module for untested code bits and write a test.

**Expected Outcomes:**
- 100 percent test coverage for the plasma module.
- Comprehensive documentation for all tests written.
