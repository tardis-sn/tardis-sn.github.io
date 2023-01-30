---
title: "2023 Ideas Page"
date: 2021-05-28T09:44:45-05:00
draft: false
layout: page
---

### Astronomy and Astrophysics Background:
A [supernova](https://en.wikipedia.org/wiki/Supernova) (here we show SN1994D in the Galaxy NGC4526 - image source: wikipedia) marks the brilliant death throes of a star, during which it outshines its entire galaxy. It not only marks death, though: supernova ejecta change the evolution of the universe and enable the formation of planets and life as we know it. From the iron in your blood to the silicon in your laptop, supernovae return heavy elements assembled from the primordial hydrogen and helium left after the big bang.

<img src="/images/480px-SN1994D.jpg" alt="image" style="display: block; margin: 0 auto;width: 80%;padding-top: 5%;padding-bottom: 5%;">
There are still many mysteries surrounding supernovae (e.g. their precise origins, inner workings, …). One way to study these objects in more detail is to split the light coming from these objects into its components (like using a prism) and analyzing the resulting data (which is called a spectrum). Here, we show spectra (black lines) of a number of different supernova types (image courtesy Daniel Kasen and LBL). Different chemical elements present in the supernova leave their mark on the spectra by imprinting characteristic features, so-called atomic lines (regions highlighted in colour). Thus, studying and interpreting such spectra allows us to identify what supernovae are made of.

<img src="/images/sn_types.jpg" alt="image" style="display: block; margin: 0 auto;width: 90;padding-top: 5%;padding-bottom: 5%;">

With sophisticated computer simulations astronomers try to reproduce the observed spectra to draw conclusion about the properties of the supernova ejecta and ultimately the explosion mechanism and progenitor stars. TARDIS is such a numerical code. It calculates theoretical spectra based on a number of input parameters, such as the supernova brightness and the abundances of the different chemical elements present in the ejecta (e.g. Oxygen, Silicon, Iron, etc.). The main idea for this procedure is that by finding a close match between theoretical and observed spectra we identify the parameters that actually describe the supernovae.

### The TARDIS Project
As mentioned in the background information above, TARDIS is a scientific tool (more specifically a Monte Carlo radiative transfer code) whose primary goal is the calculation of theoretical spectra for supernovae. Below, you find the typical result of a TARDIS calculation. It shows the calculated synthetic spectra for a simple supernova model. This particular setup (tardis_example) is officially provided by the TARDIS collaboration on the [documentation](https://tardis-sn.github.io/tardis/).
<img src="/images/tardis_example.png" alt="image" style="display: block; margin: 0 auto;width: 90%;padding-top: 5%;padding-bottom: 5%;">

### List of GSoC 2023 Project Ideas
In the TARDIS collaboration we first establish a detailed plan on implementing new features before starting the actual work. This is an important step that ensures that the entire TARDIS collaboration is informed about the development efforts and that the team members can help shape the ideas during the discussion phase. We call these documents TEP - TARDIS Enhancement Proposals. We already have a great list of ideas [here](https://github.com/tardis-sn/tep) that we need help with. Some of these we have specially selected for GSoC 2023 and are listed with specific “warm-up” tasks below. But feel free to propose your own TEP and make a PR on that.

If you use one of our TEPs, you can definitely add more detail to the implementation, but what we really want to see is a detailed timeline with milestones that shows us that you have thought about how to implement the feature in three months. For any questions about the projects, please ask on [Gitter](https://gitter.im/tardis-sn/gsoc).

Putting in a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request) with the First objective is essential for each proposal to allow to see how you work.


#### Grotrian diagram visualisation
**Project Length:** 350 Hours\
**Difficulty:** Moderate\
**Astronomy knowledge needed**: Basic atomic physics\
**Mentors:** Mark Mage, Atharva Arya\
**Programming skills required:** Python, GitHub, Matplotlib and/or plotly\
**Description:** TARDIS generates synthetic observations of stellar explosions that can be compared to real observations. With such comparisons, we can learn more about the physical processes occurring and the conditions inside the supernova, including which elements and atomic transitions are dominant. TARDIS tracks the atomic transitions of interacting photons, level populations, etc. allowing the user to interrogate the physical conditions of the supernova. The goal of this project is to build a visual tool to represent this information for the user in Grotrian diagrams, which show different atomic levels of ions and transitions between them. An example is shown here from Boyle et al. 2017. Developing this tool will allow the user to more easily understand the important physical conditions of their supernova model.
<img src="/images/Grotrian.png" alt="image" style="display: block; margin: 0 auto;width: 100%;padding-top: 5%;padding-bottom: 5%;">
**Your first objective if you choose to accept the mission:** Run a TARDIS simulation and plot the fraction of neutral and singly-ionised silicon against velocity.


#### Inner boundary velocity solver
**Project Length:** 350 Hours\
**Difficulty:** Hard\
**Astronomy knowledge needed**: Some general understanding of thermodynamics and numerical calculus\
**Mentors:** Jack O'Brien\
**Programming skills required:** Git, Python, NumPy, Pandas\
**Description:** TARDIS operates on a "photospheric" inner boundary approximation.  A hard inner boundary in velocity is set from which radiative packets are emitted through the ejecta according to a black-body distribution at a given temperature.  Currently, TARDIS can solve for the radiative and inner boundary temperatures as well as dilution factors given a static inner velocity boundary.  The precise location of where this inner boundary velocity should be placed is not always obvious and there are a few methods by which one can intelligently select a location based on the properties of the plasma (which are constantly updating over each iteration).  We would like to be able to update the location of the inner boundary velocity at each iteration based on a set of options for desired properties of the plasma at each iteration so that the inner boundary velocity does not have to be set by hand.  The options include setting the inner boundary velocity according to a given optical depth over all frequencies (either Planck or Rossland mean opacities) or setting the inner boundary according to a desired value for the dilution factors.  Some work must be done to handle these updates mid iteration as the updated velocity boundary may, for example, move outside the bounds of the simulation or may move between simulation shells.  
**First objective:** In a jupyter notebook, run a TARDIS simulation then use the electron densities and Sobolev optical depths (tau_sobolevs) to compute the Planck mean opacity for the simulation as a function of velocity.  Post this notebook with the plot in a pull request on github.


#### Develop an interactive abundance visualisation tool
**Difficulty:** Easy\
**Astronomy knowledge needed:** None\
**Mentors:** James Gillanders\
**Programming skills required:** Python, Github, Matplotlib, Plotly\
**Description:** TARDIS is used to model and understand the properties of the material ejected during violent explosions in space. By specifying some input model parameters, the simulation runs and generates synthetic spectra which can be compared to observations. Currently, some of the model properties can be difficult to interpret, and so we envisage developing some helpful visualisation tools to aid in understanding the properties of the input model. Specifically, we hope to develop an interactive widget that illustrates the composition of the ejected material across the velocity of the simulation. The focus of this project would be developing a TARDIS plot that is inspired by the TULIPS visualisation tools (see https://astro-tulips.readthedocs.io/en/latest/chemical_profile_diagram.html).
<img src="/images/tulips_chemical_profile.png" alt="image" style="display: block; margin: 0 auto;width: 100%;padding-top: 5%;padding-bottom: 5%;">

#### STARDIS Parallelization and GPU
**Project Length:** 350 Hours\
**Difficulty:** Difficult\
**Astronomy knowledge needed**: None, knowledge about stars is recommended\
**Mentors:** Isaac Smith, Jaladh Singhal\
**Programming skills required:** Python, GitHub, Numba and CUDA\
**Description:** STARDIS generates synthetic spectra for stars, given a set of parameters. These spectra can then be compared to real observations to give us information about the conditions inside that star’s atmosphere. STARDIS is a new companion code to TARDIS, and has not yet been optimised. The goal of this project is to increase the speed of STARDIS using [Numba](https://numba.readthedocs.io/en/stable/index.html) by allowing slower parts of STARDIS to be run [in parallel](https://numba.readthedocs.io/en/stable/user/parallel.html), and allowing for them to be run on the GPU using Numba’s [CUDA capabilities](https://numba.readthedocs.io/en/stable/cuda/index.html). As a reference, this has been done in TARDIS with the formal integral. The regular Numba version (with parts parallelized) can be found [here](https://github.com/tardis-sn/tardis/blob/master/tardis/montecarlo/montecarlo_numba/formal_integral.py). Then, there is also a version written with CUDA [here](https://github.com/tardis-sn/tardis/blob/master/tardis/montecarlo/montecarlo_numba/formal_integral_cuda.py). Increasing the speed of STARDIS will allow research to be done rapidly using our tools.

**First objective:** 