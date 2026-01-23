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
   - [Rewrite the TARDIS visualisation module using Panel](#rewrite-the-tardis-visualisation-module-using-panel)


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

#### Rewrite the TARDIS visualisation module using Panel

{{<idea_tag "Panel">}} {{<idea_tag "Visualisation">}}

<img src="/gsoc_2025/panel.png" alt="image" style="display: block; margin: 0 auto;width: 50%;padding-top: 5%;padding-bottom: 5%;">

**Project Length:** 350 Hours \
**Difficulty:** Hard \
**Mentors:** Andrew Fullard, Atharva Arya, James Gillanders \
**Description:** TARDIS has a collection of visualisation tools and widgets to interactively explore TARDIS simulations which run inside Jupyter Notebooks. A lot of these modules currently depend on dependencies like ipywidgets which do not work well with our Sphinx documentation. Some of these tools have already been migrated but we want to migrate the rest of our widgets to panel too.

Visualisation Module-
https://tardis-sn.github.io/tardis/pull/2872/io/visualization/index.html#tardis-widgets-graphical-user-interfaces

**First Objective:** The line info and shell info widgets are already migrated to panel but they are not fully interactive on the documentation. Make them work as they work in the notebooks.

**Expected Outcomes:**
- All visualisation modules moved to Panel.
- Visualisation tools and widgets can be embedded on the website allowing users to interact with them.
- Comprehensive documentation and tests for all code written.
