---
title: A Sample of TARDIS Improvements at TARDISCon
excerpt: >-
  At TARDISCon, we developed two new sampling methods for different scenarios:- the decay of positronium and the emission of packets from the photosphere.
publishDate: 2024-07-19
thumb_image: ../articles/samplers_compare.gif
seo:
  title: A Sample of TARDIS Improvements at TARDISCon
  description: At TARDISCon, we developed two new sampling methods for different scenarios:- the decay of positronium and the emission of packets from the photosphere.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: A Sample of TARDIS Improvements at TARDISCon
      keyName: property
    - name: 'og:description'
      value: >-
        At TARDISCon, we developed two new sampling methods for different scenarios:- the decay of positronium and the emission of packets from the photosphere.
      keyName: property
    - name: 'og:image'
      value: ../articles/samplers_compare.gif
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: A Sample of TARDIS Improvements at TARDISCon
    - name: 'twitter:description'
      value: >-
        At TARDISCon, we developed two new sampling methods for different scenarios:- the decay of positronium and the emission of packets from the photosphere.
    - name: 'twitter:image'
      value: ../articles/samplers_compare.gif
      relativeUrl: true
layout: post
---

At TARDISCon, part of the TARDIS team (Anirban Dutta, Jing Lu, and Jack O’Brien) worked on a new positronium spectrum sampler. Positronium is a bound system of an electron and a positron that is stable for only a very short time (nanoseconds). It has a chance to be formed as part of the beta decay process of radioactive elements in supernovae. When the electron-positron pair annihilate each other, they can produce either 2 or 3 gamma-rays. We wrote code to sample the possible gamma-ray energies by inverting the integral description from Ore & Powell (1949).

This sampler will be used as part of the gamma-ray energy deposition module for TARDIS that is currently under development. It will enable TARDIS to accurately simulate the formation and annihilation of positronium and the resulting gamma-ray spectra and deposition rates.

In addition to adding samplers for new physics processes, TARDIS team members added new sampling features to the existing radiative transfer framework.  Jack O'Brien, Anirban Dutta, and Wolfgang Kerzendorf wrote a weighted sampler implementation for the Monte Carlo packet instantiation.  This new sampler allows TARDIS to draw more packet samples in wavelength regions with low radiative intensity to improve the quality of the statistics, especially near the red and blue ends of the spectrum.  In contrast to the original packet sampler, which generates packets at each frequency with a probability corresponding to its initial radiative intensity, the weighted sampler works by drawing frequencies for each packet uniformly across the spectrum and assigning a weight to each packet based on the initial radiative intensity.  In the future, this sampler will serve to help TARDIS both track and actively improve its sampling efficiency in undersampled regions of the spectrum as well as serve as a base for more complex importance samplers.


