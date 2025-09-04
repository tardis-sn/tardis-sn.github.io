---
title: Introducing STARDIS - An Open and Modular Stellar Spectral Synthesis Code
excerpt: >-
  We introduce STARDIS, a new open-source Python stellar spectral synthesis code that performs 1D LTE radiative transfer for FGK stars from near-UV to IR wavelengths.
publishDate: 2025-08-28
thumb_image: ../articles/halpha_sol.png
seo:
  title: Introducing STARDIS - An Open and Modular Stellar Spectral Synthesis Code
  description: We introduce STARDIS, a new open-source Python stellar spectral synthesis code that performs 1D LTE radiative transfer for FGK stars from near-UV to IR wavelengths.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Introducing STARDIS - An Open and Modular Stellar Spectral Synthesis Code
      keyName: property
    - name: 'og:description'
      value: >-
        We introduce STARDIS, a new open-source Python stellar spectral synthesis code that performs 1D LTE radiative transfer for FGK stars from near-UV to IR wavelengths.
      keyName: property
    - name: 'og:image'
      value: ../articles/halpha_sol.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Introducing STARDIS - An Open and Modular Stellar Spectral Synthesis Code
    - name: 'twitter:description'
      value: >-
        We introduce STARDIS, a new open-source Python stellar spectral synthesis code that performs 1D LTE radiative transfer for FGK stars from near-UV to IR wavelengths.
    - name: 'twitter:image'
      value: ../articles/halpha_sol.png
      relativeUrl: true
layout: post
---

We are excited to announce the release of STARDIS, a new 1D stellar spectral synthesis Python code with a detailing manuscript published in The Astrophysical Journal. STARDIS is a modular, open-source radiative transfer code capable of spectral synthesis from near-UV to IR for FGK stars. Built on the TARDIS infrastructure and written in Python—one of the most used languages in astronomy—STARDIS is intended to be approachable for current and future astrophysicists.

<img src='\../articles/stardis_diagram.jpeg' alt='Image'>

The code performs three major computational steps: solving the plasma state (molecular, ionization, and excitation balances), calculating wavelength-dependent opacities including continuum and line sources with sophisticated broadening treatments, and solving the radiative transfer equation through ray-tracing to produce synthetic stellar spectra. Validation against established codes like KORG shows excellent agreement, typically within 3% for most spectral features, making STARDIS a reliable tool for stellar abundance analysis and spectroscopic studies.


