---
title: "GSoC 2024 Ideas"
date:
draft: false
layout: page
---

### Astronomy and Astrophysics Background:

A [supernova](https://en.wikipedia.org/wiki/Supernova) (here we show SN1994D in the Galaxy NGC4526 - image source: wikipedia) marks the brilliant death throes of a star, during which it outshines its entire galaxy. It not only marks death, though: supernova ejecta change the evolution of the universe and enable the formation of planets and life as we know it. From the iron in your blood to the silicon in your laptop, supernovae return heavy elements assembled from the primordial hydrogen and helium left after the big bang.

<img src="/images/480px-SN1994D.jpg" alt="image" style="display: block; margin: 0 auto;width: 70%;padding-top: 5%;padding-bottom: 5%;">
There are still many mysteries surrounding supernovae (e.g. their precise origins, inner workings, …). One way to study these objects in more detail is to split the light coming from these objects into its components (like using a prism) and analyzing the resulting data (which is called a spectrum). Here, we show spectra (black lines) of a number of different supernova types (image courtesy Daniel Kasen and LBL). Different chemical elements present in the supernova leave their mark on the spectra by imprinting characteristic features, so-called atomic lines (regions highlighted in colour). Thus, studying and interpreting such spectra allows us to identify what supernovae are made of.

<img src="/images/sn_types.jpg" alt="image" style="display: block; margin: 0 auto;width: 70%;padding-top: 5%;padding-bottom: 5%;">

With sophisticated computer simulations astronomers try to reproduce the observed spectra to draw conclusion about the properties of the supernova ejecta and ultimately the explosion mechanism and progenitor stars. TARDIS is such a numerical code. It calculates theoretical spectra based on a number of input parameters, such as the supernova brightness and the abundances of the different chemical elements present in the ejecta (e.g. Oxygen, Silicon, Iron, etc.). The main idea for this procedure is that by finding a close match between theoretical and observed spectra we identify the parameters that actually describe the supernovae.

### The TARDIS Project

As mentioned in the background information above, TARDIS is a scientific tool (more specifically a Monte Carlo radiative transfer code) whose primary goal is the calculation of theoretical spectra for supernovae. Below, you find the typical result of a TARDIS calculation. It shows the calculated synthetic spectra for a simple supernova model. This particular setup (tardis_example) is officially provided by the TARDIS collaboration on the [documentation](https://tardis-sn.github.io/tardis/).
<img src="/images/tardis_example.png" alt="image" style="display: block; margin: 0 auto;width: 70%;padding-top: 5%;padding-bottom: 5%;">

### List of GSoC 2024 Project Ideas

In the TARDIS collaboration we first establish a detailed plan on implementing new features before starting the actual work. This is an important step that ensures that the entire TARDIS collaboration is informed about the development efforts and that the team members can help shape the ideas during the discussion phase. We call these documents TEP - TARDIS Enhancement Proposals. We already have a great list of ideas [here](https://github.com/tardis-sn/tep) that we need help with. Some of these we have specially selected for GSoC 2024 and are listed with specific “warm-up” tasks below. But feel free to propose your own TEP and make a PR on that.

If you use one of our TEPs, you can definitely add more detail to the implementation, but what we really want to see is a detailed timeline with milestones that shows us that you have thought about how to implement the feature in three months. For any questions about the projects, please ask on [Gitter](https://gitter.im/tardis-sn/gsoc).

Putting in a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) with the First objective is essential for each proposal to allow to see how you work.

#### TARDIS Benchmarking

{{<idea_tag "Python">}} {{<idea_tag "GitHub">}} {{<idea_tag "Benchmarking">}}

**Project Length:** ~175 Hours\
**Difficulty:** Moderate\
**Mentors:** Andrew Fullard, Atharva Arya, Aoife Boyle\
**Description:** TARDIS uses [Airspeed Velocity](https://asv.readthedocs.io/en/stable/) to produce benchmarks that measure the performance of TARDIS. These benchmarks are created via a [GitHub Action](https://github.com/tardis-sn/tardis/blob/master/.github/workflows/benchmarks.yml) that runs whenever a commit is made to the main branch. It will also trigger when a benchmarks label is added to pull requests, and produce a bot comment that lists the benchmark results.

Currently, the benchmarks for the previous 5 commits are created and pushed to a [separate repository](https://github.com/tardis-sn/tardis-benchmarks/tree/main). This repository publishes to a [website](https://tardis-sn.github.io/tardis-benchmarks/).

We would like you, the GSoC contributor for this project, to improve the benchmarking system for TARDIS. You should plan to expand the framework to make it easy for us to add benchmarks to different parts of TARDIS. You should improve the GitHub Action to store more than just the recent 5 commits of benchmarks to provide an extended history. You should use the improved framework to add more benchmarks that cover other areas of the TARDIS code. You could improve the Airspeed Velocity page to better represent the existing benchmark.\
**First objective:** Create a new benchmark for an isolated part of TARDIS using Airspeed Velocity. We recommend looking at the existing benchmark and unit tests for inspiration.

<img src="/images/tardis_benchmarking.png" alt="image" style="display: block; margin: 0 auto;width: 70%;padding-top: 5%;padding-bottom: 5%;">

#### TARDIS Benchmarking and Performance Improvement

{{<idea_tag "GitHub">}} {{<idea_tag "Benchmarking">}} {{<idea_tag "Performance">}}

**Project Length:** Large, ~350 Hours\
**Difficulty:** Hard\
**Mentors:** Andrew Fullard, Atharva Arya, Alex Holas\
**Description:** This project aims to enhance the efficiency and scalability of the TARDIS radiative transfer code, a critical tool in astrophysical simulations. TARDIS is widely used for modeling the spectra of astronomical transients, providing valuable insights into complex physical processes.\
However, as computational demands increase and simulations grow in complexity, identifying and addressing performance bottlenecks becomes imperative. The primary goals of this project are to investigate potential performance bottlenecks within the TARDIS codebase, optimize critical components, and establish robust benchmarking procedures. The first half of this project will consist of the “TARDIS Benchmarking” project listed above. The second part will involve making changes to parts of TARDIS identified as poorly performing.\
The project will focus on improving both single- and multi-core performance and scaling to ensure that TARDIS remains a reliable and efficient tool for researchers in the field. During this project you will acquire hands-on experience with state-of-the-art profiling tools such as [memray](https://github.com/bloomberg/memray), gaining a deep understanding of how to identify and analyze performance bottlenecks in complex codebases like TARDIS. Furthermore you will work closely with the TARDIS codebase, enhancing your ability to navigate and understand intricate scientific software. This experience is invaluable for anyone interested in contributing to large-scale computational projects.\
By the end of the project, you will not only have made significant contributions to TARDIS but will have acquired a versatile skill set that is transferable to various domains within computational science and software engineering.\
**First objective**:
Create a new benchmark for an isolated part of TARDIS using [Airspeed Velocity](https://asv.readthedocs.io/en/stable/). We recommend looking at the existing benchmark and unit tests for inspiration.\
AND\
Create a memory usage profile of the TARDIS example simulations using a tool such as [memray](https://github.com/bloomberg/memray).

#### Velocity Packet Tracker Visualization

{{<idea_tag "Python">}} {{<idea_tag "GitHub">}} {{<idea_tag "Matplotlib">}} {{<idea_tag "Plotly">}}

**Project Length:** 175 Hours\
**Difficulty:** Moderate\
**Mentors:** James Gillanders, Jing Lu, Harshul Gupta, Jaladh Singhal

**Description:**
The TARDIS SDEC plot visualizes which elements contribute towards the absorption and emission features of the output spectrum. However, the SDEC plot does not visualize where these interactions occur within the ejecta. This information can be extremely useful to astronomers who want to understand which regions of the ejecta are responsible for important features in the output spectrum. This project will develop a visualization tool that plots the number of photon packet interactions as a function of velocity for each element present in the ejecta. See this pull request for an example of what the plot could look like: https://github.com/tardis-sn/tardis/pull/1606.

**First objective:**\
· Install the most up-to-date version of the TARDIS code.\
· Run the example simulation and generate an SDEC plot.\
· Make a plot showing the abundance of each element, as a function of velocity.\
· Make a plot that illustrates the total number of interactions that escape the simulation from the different elements.

<img src="/images/velocity_tracker.png" alt="image" style="display: block; margin: 0 auto;width: 70%;padding-top: 5%;padding-bottom: 5%;">

#### Parallelization and GPU

{{<idea_tag "Python">}} {{<idea_tag "GitHub">}} {{<idea_tag "Numba">}} {{<idea_tag "Cuda">}}

**Project Length:** 175 Hours\
**Mentors:** Wolfgang Kerzendorf, Josh Shields \
**Difficulty:** Moderate\
**Description:** STARDIS generates synthetic spectra for stars, given a set of parameters. These spectra can then be compared to real observations to give us information about the conditions inside that star’s atmosphere. STARDIS is a new companion code to TARDIS, and has not yet been optimised. The goal of this project is to increase the speed of STARDIS using [Numba](https://numba.readthedocs.io/en/stable/index.html) by allowing slower parts of STARDIS to be run [in parallel](https://numba.readthedocs.io/en/stable/user/parallel.html), and allowing for them to be run on the GPU using Numba’s [CUDA capabilities](https://numba.readthedocs.io/en/stable/cuda/index.html) or [CuPY](https://cupy.dev/). As a reference, this has been done in TARDIS with the formal integral. The regular Numba version (with parts parallelized) can be found [here](https://github.com/tardis-sn/tardis/blob/master/tardis/montecarlo/montecarlo_numba/formal_integral.py). Then, there is also a version written with CUDA [here](https://github.com/tardis-sn/tardis/blob/master/tardis/montecarlo/montecarlo_numba/formal_integral_cuda.py). Increasing the speed of STARDIS will allow research to be done rapidly using our tools.

**First objective:** In the TARDIS repository, find the Jupyter Notebook that creates the [initialization page of the documentation](https://tardis-sn.github.io/tardis/physics/montecarlo/initialization.html). Create a version of `planck_function()` (see code cell #6) that is `jit` compiled by Numba. Show a comparison of how long it takes to calculate `planck_function(nus_planck)` (see code cell #7) for the original function versus the `jitted` function for 100, 200, and 500 frequency bins. Make a pull request to the TARDIS repository with your modifications of this notebook.

#### Enhancing TARDIS Packet Tracker

{{<idea_tag "Python">}} {{<idea_tag "Numba">}} {{<idea_tag "Pandas">}}

**Project Length:** 350 Hours\
**Mentors:** Wolfgang Kerzendorf, Christian Vogl \
**Difficulty:** Moderate\
**Description:** TARDIS has a lot of monitoring functionality to study the interiors of the exploding star. At the heart of the current implementation is a so-called packet tracker that logs how the energy escapes the supernovae. In this project, we want to bring together several legacy techniques to track the packets by enhancing the main tracker.
[The tracker](https://tardis-sn.github.io/tardis/io/output/rpacket_tracking.html) can be initialized in the configuration and will produce pandas Dataframes of the packet interaction. Currently, the level of tracking and monitoring is fixed and we want to make the tracker able to be able to track the packets with different detail levels. The addition to the tracking detail will require changes to the compiled part of the Python code (we use the [Numba](https://numba.readthedocs.io/) package for high-performance implementation. The project will give you a very good insight into high-performance and Just-In-Time compiled python and how to connect it to the rest of a larger python project.

**First objective:** Follow the [instructions](https://tardis-sn.github.io/tardis/io/output/rpacket_tracking.html) to setup the tracking for an example TARDIS run. Read-up on how to change the interaction_type column to a category column. Change the documentation notebook and make a Pull Request on that change. Think about how you would track only the last interaction of the packets.
