---
title: "GSoC 2025 Ideas"
date: 2025-02-01
draft: false
layout: page
aliases:
    - /gsoc/ideas
---

## Table of Contents

1. [Astronomy and Astrophysics Background](#astronomy-and-astrophysics-background)
2. [The TARDIS Project](#the-tardis-project)
3. [List of GSoC 2025 Project Ideas](#list-of-gsoc-2025-project-ideas)
   - [Rewrite the TARDIS visualisation module using Panel](#rewrite-the-tardis-visualisation-module-using-panel)
   - [Line Identification Plotting Functionality](#line-identification-plotting-functionality)
   - [Regression Data Dashboard](#regression-data-dashboard)
   - [Adding HDF Writing Capabilities to TARDIS Modules](#adding-hdf-writing-capabilities-to-tardis-modules)
   - [Benchmark Optimization](#benchmark-optimization)
   - [Metadata for atomic data](#metadata-for-atomic-data)
   - [Continuum opacity source reader](#continuum-opacity-source-reader)
   - [CARSUS Dashboard](#carsus-dashboard)


### Astronomy and Astrophysics Background:

A <a href="https://en.wikipedia.org/wiki/Supernova" target="_blank">supernova</a>(here we show SN1994D in the Galaxy NGC4526 - image source: wikipedia) marks the brilliant death throes of a star, during which it outshines its entire galaxy. It not only marks death, though: supernova ejecta change the evolution of the universe and enable the formation of planets and life as we know it. From the iron in your blood to the silicon in your laptop, supernovae return heavy elements assembled from the primordial hydrogen and helium left after the big bang.

<img src="/images/480px-SN1994D.jpg" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">
There are still many mysteries surrounding supernovae (e.g. their precise origins, inner workings, …). One way to study these objects in more detail is to split the light coming from these objects into its components (like using a prism) and analyzing the resulting data (which is called a spectrum). Here, we show spectra (black lines) of a number of different supernova types (image courtesy Daniel Kasen and LBL). Different chemical elements present in the supernova leave their mark on the spectra by imprinting characteristic features, so-called atomic lines (regions highlighted in colour). Thus, studying and interpreting such spectra allows us to identify what supernovae are made of.

<img src="/images/sn_types.jpg" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

With sophisticated computer simulations astronomers try to reproduce the observed spectra to draw conclusion about the properties of the supernova ejecta and ultimately the explosion mechanism and progenitor stars. TARDIS is such a numerical code. It calculates theoretical spectra based on a number of input parameters, such as the supernova brightness and the abundances of the different chemical elements present in the ejecta (e.g. Oxygen, Silicon, Iron, etc.). The main idea for this procedure is that by finding a close match between theoretical and observed spectra we identify the parameters that actually describe the supernovae.

### The TARDIS Project

As mentioned in the background information above, TARDIS is a scientific tool (more specifically a Monte Carlo radiative transfer code) whose primary goal is the calculation of theoretical spectra for supernovae. Below, you find the typical result of a TARDIS calculation. It shows the calculated synthetic spectra for a simple supernova model. This particular setup (tardis_example) is officially provided by the TARDIS collaboration on the <a href="https://tardis-sn.github.io/tardis/" target="_blank">documentation</a>.
<img src="/images/tardis_example.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

### List of GSoC 2025 Project Ideas

In the TARDIS collaboration we first establish a detailed plan on implementing new features before starting the actual work. This is an important step that ensures that the entire TARDIS collaboration is informed about the development efforts and that the team members can help shape the ideas during the discussion phase. We call these documents TEP - TARDIS Enhancement Proposals. We already have a great list of ideas <a href="https://github.com/tardis-sn/tep" target="_blank">here</a> that we need help with. Some of these we have specially selected for GSoC 2025 and are listed with specific “warm-up” tasks below. But feel free to propose your own TEP and make a PR on that.

If you use one of our TEPs, you can definitely add more detail to the implementation, but what we really want to see is a detailed timeline with milestones that shows us that you have thought about how to implement the feature in three months. For any questions about the projects, please ask on <a href="https://gitter.im/tardis-sn/gsoc" target="_blank">Gitter</a>.

Putting in a <a href="https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request" target="_blank">Pull Request</a> with the First objective is essential for each proposal to allow to see how you work.

#### Rewrite the TARDIS visualisation module using Panel

{{<idea_tag "Panel">}} {{<idea_tag "Visualisation">}}

<img src="/gsoc_2025/panel.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Hard \
**Mentors:** Abhinav Ohri, Andrew Fullard, Atharva Arya, James Gillanders \
**Description:** TARDIS has a collection of visualisation tools and widgets to interactively explore TARDIS simulations which run inside Jupyter Notebooks. A lot of these modules currently depend on dependencies like IPython and Qgrid which do not work well with our Sphinx documentation. We want to migrate our tools to depend entirely on Panel instead of these tools and want to showcase their interactivity on our documentation.

Visualisation Module- 
https://tardis-sn.github.io/tardis/pull/2872/io/visualization/index.html#tardis-widgets-graphical-user-interfaces 

**First Objective:** Use Panel to show any hierarchical dataset as 2 interlinked tables, where selecting a row in the first table updates the 2nd table with the data corresponding to the selected row. Bonus points for using TARDIS’ [SimulationShellInfo](https://github.com/tardis-sn/tardis/blob/master/tardis/visualization/widgets/shell_info.py#L177) to make the 1st table display shell data and the 2nd table display element abundances.

**Expected Outcomes:**
- All visualisation modules moved to Panel.
- Dependencies like qgrid/qgridnext removed. 
- Visualisation tools and widgets can be embedded on the website allowing users to interact with them.
- Comprehensive documentation and tests for all code written.


#### Line Identification Plotting Functionality

{{<idea_tag "Visualisation">}} {{<idea_tag "Plotly">}} {{<idea_tag "Matplotlib">}} 

<img src="/gsoc_2025/line_identification.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 hours\
**Difficulty:** Medium\
**Mentors:** Abhinav Ohri, Andrew Fullard, James Gillanders

**Description:**
TARDIS and STARDIS produce spectra that contain information about the elements and molecules that are part of the simulation. Both software record information about which elements produce which parts of the output spectrum. For TARDIS and STARDIS, you will access the information about where lines originate and plot the frequencies or wavelengths of the originating elements or molecules as requested by the user. This functionality will be incorporated into any of the existing spectral visualizations in TARDIS and STARDIS, so it must be modular. 

**First Objective:**
Produce a table of energy packets that can be filtered by the originating element. Provide a Jupyter notebook showing a plot of the table with labels and style that matches other TARDIS visualizations.

**Expected Outcomes:**
- Visualisation Module that builds the plot using existing dependencies.  
- Comprehensive documentation and tests for all code written.



#### Regression Data Dashboard

{{<idea_tag "Data Visualisation">}} {{<idea_tag "Dashboards">}} {{<idea_tag "Python">}} {{<idea_tag "Git">}} {{<idea_tag "HDF">}}

**Project Length:** 350 Hours \
**Difficulty:** Hard \
**Mentors:** Abhinav Ohri, Andrew Fullard, Atharva Arya

**Description:**
TARDIS implements a regression testing framework that compares current output to an already saved version to validate code. The goal of this project is to develop a dashboard to see exactly where the values of the files changed. Other than this, this project will also improve TARDIS HDF writing capabilities and add functionality to restore simulations from HDF and to create simulation checkpoints which work with the regression data. 

TARDIS Regression Data: https://github.com/tardis-sn/tardis-regression-data 

**First objective:**\
[Run the comparison notebook](https://github.com/tardis-sn/tardis-regression-data/blob/main/compare_regression_data.ipynb) for the past 10 TARDIS commits and share a graph of how any file changed over the course of these commits. Hint: Each TARDIS commit will generate its own regression data that you need to compare to the data the previous commit produced.

**Expected Outcomes:**
- Dashboard preferably using existing TARDIS dependencies(see Conda environment)
- Visualisation that allows seeing how regression data files changed over a large commit range. Commits which produce large changes are recorded permanently.
- Flexible code that works with changes in the TARDIS environment.
- Comprehensive documentation and tests for all code written.



#### Adding HDF Writing Capabilities to TARDIS Modules 

{{<idea_tag "Data Storage">}} {{<idea_tag "HDF5">}} {{<idea_tag "Python">}}

**Project Length:** 350 Hours \
**Mentors:** Andrew Fullard, Atharva Arya, Abhinav Ohri \
**Difficulty:** Hard \
**Description:** This project will improve TARDIS HDF writing capabilities and add functionality to restore simulations from HDF and to create simulation checkpoints which work with the regression data.

TARDIS Regression Data: https://github.com/tardis-sn/tardis-regression-data 

**First objective:** Add a method to the [spectrum class](https://github.com/tardis-sn/tardis/blob/304154a270a5270d5e575e901c7b1d794a8e2511/tardis/spectrum/spectrum.py#L9) that allows restoring the class from an HDF. Share the notebook in a pull request.

**Expected Outcomes:**
- Modular code that allows recreating TARDIS modules from HDF files exactly the way they were before. 
- Comprehensive documentation and tests for all code written.



#### Benchmark Optimization

{{<idea_tag "Performance">}} {{<idea_tag "Benchmarking">}} {{<idea_tag "Python">}} {{<idea_tag "Airspeed Velocity">}}

<img src="/gsoc_2025/benchmark.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Mentors:** Andrew Fullard, Atharva Arya, Abhinav Ohri \
**Difficulty:** Hard \
**Description:** TARDIS commits are monitored by a benchmarking framework to detect performance regressions. But the current framework only tests 5 commits at a time and not with much detail. The goal of this project is to improve the benchmarking framework by adding more benchmarks. This project will also add more benchmarks to STARDIS, a related code. The second stage of the project will use the benchmarks to investigate possible performance improvements to TARDIS and STARDIS.

- TARDIS Benchmarks: https://tardis-sn.github.io/tardis-benchmarks/
- STARDIS  Benchmarks: https://tardis-sn.github.io/stardis-benchmarks/

**First objective:** Benchmark the [Plasma solver factory](https://github.com/tardis-sn/tardis/blob/304154a270a5270d5e575e901c7b1d794a8e2511/tardis/plasma/assembly/base.py#L46) and share the ASV results for the last 5 commits along with the code in a pull request.

**Expected Outcomes:**
- Exhaustive benchmarks that time important TARDIS modules like plasma, transport, visualisation to name a few.
- Larger history of benchmarks(currently only 5) and regenerating benchmarks for failed commits to avoid losing benchmark history. 
- Comprehensive documentation and tests for all code written.



#### Metadata for atomic data

{{<idea_tag "Data Management">}} {{<idea_tag "Atomic Data">}} {{<idea_tag "Pandas">}}

<img src="/gsoc_2025/carsus1.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

<img src="/gsoc_2025/carsus2.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Mentors:** Andreas Flörs, Andrew Fullard \
**Difficulty:** Easy \
**Description:** Carsus provides atomic data to astrophysicists. It would be useful to provide additional data, “metadata”, along with the atomic data, so that users know the source and details of how the data were processed. For this project, you will add metadata to the Carsus atomic data output. This metadata will include physical units, git commit hashes, article citations, and more. You will also work on TARDIS to enable reading of this metadata.

Carsus- https://tardis-sn.github.io/carsus/ 

**First objective:** add a metadata table to an existing Carsus output, with a DOI link to a journal article of your choice, some physical units (e.g. Hertz, meters, erg). The output could be the Carsus HDF file, or a Pandas DataFrame. Some form of automation is a bonus.


**Expected Outcomes:**
- Metadata for all Carsus outputs.
- Comprehensive documentation and tests for all code written.



#### Continuum opacity source reader

{{<idea_tag "Data Processing">}} {{<idea_tag "Scientific Data">}}

<img src="/gsoc_2025/carsus3.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Mentors:** Andrew Fullard, Josh Shields \
**Difficulty:** Hard \
**Description:** There’s a lot of literature with useful tables for the TARDIS codebase and other scientific codes in pdfs ([example](https://academic.oup.com/mnras/article/266/4/805/982644)), or often in dataproducts. Carsus currently reads in data from standard sources and archives([Chianti](https://www.chiantidatabase.org/), [CMFGEN](https://sites.pitt.edu/~hillier/web/CMFGEN.htm) ), but does not flexibly read data from sources in the literature. The goal of this project is to expand Carsus to read datatables like ones in this work, with potential expansion for a future-proof workflow (new opacity tables). These could all go in a new tardis repository called “carsus-literature-tables” or something along those lines. You can look at [this](https://github.com/tardis-sn/carsus-data-molecules-barklem2016) for a preprocessed datatables ready to be ingested by Carsus might look.

Carsus- https://tardis-sn.github.io/carsus/ 

**First objective:** Read one of the datatables from the linked paper [here](https://cdsarc.cds.unistra.fr/viz-bin/cat/VI/80#/browse) (try s92.201.gz, under ftp) and process it into a pandas dataframe. Look to do this in a programmatic way that could be reused for similar files, like the other tables found here. See [section 6.4](https://articles.adsabs.harvard.edu/pdf/1994MNRAS.266..805S) for more details on table contents and formatting if desired.


**Expected Outcomes:**
- Code that reads in the new dataproducts and integrates with Carsus.
- Comprehensive documentation and tests for all code written.



#### CARSUS Dashboard

{{<idea_tag "GitHub Actions">}} {{<idea_tag "Python Scripting">}} {{<idea_tag "Pandas">}} {{<idea_tag "Notebooks">}}

<img src="/gsoc_2025/carsus_dashboard.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Mentors:** Josh Shields \
**Difficulty:** Hard \
**Description:** Carsus is a package to manage atomic datasets. It can read data from a variety of sources and output them to file formats readable by radiative transfer codes like TARDIS. The goal of this project is to build python APIs and Jupyter Notebook scripts to investigate different atomic datasets from various sources. The scripts help researchers analyze key components of atomic data files, including metadata, lines/levels structure and element composition, while enabling web access to examine and compare different atomic datasets.

- Regression Data Repository: https://github.com/tardis-sn/tardis-regression-data 
- Carsus: https://github.com/tardis-sn/carsus 


**First objective:** Use Jinja2 to generate an HTML Report that investigates an atomic file. Display top 50 rows of levels and lines dataframes from the atomic file for Silicon. 
Here are a few example notebooks-
- [Quickstart Notebook](https://tardis-sn.github.io/carsus/quickstart.html) 
- [Compare atomic files](https://tardis-sn.github.io/carsus/development/compare_atomic_files.html). You can find atomic files in the [TARDIS regression data repository](https://github.com/tardis-sn/tardis-regression-data)


**Expected Outcomes:**
- Python APIs and notebooks that investigate custom atomic data files from external parameters and can be triggered using GitHub Actions.
- Modular code that is compatible with both legacy atom data files and is future-proof.
- Comprehensive documentation and tests for all code written.
