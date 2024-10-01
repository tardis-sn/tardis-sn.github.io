---
title: LIV (Last Interaction Velocity) Plot
excerpt: >-
  Hi, this article highlights the development of the LIV (Last Interaction Velocity) Plot during this summer's GSoC program—a new visualization tool that plots the last photon packet interactions by velocity for each element in supernova ejecta, offering deeper insights into supernova spectra.
publishDate: 2024-08-23
thumb_image: ../articles/LIV_ply.png
seo:
  title: LIV (Last Interaction Velocity) Plot
  description: Hi, this article highlights the development of the LIV (Last Interaction Velocity) Plot during this summer's GSoC program—a new visualization tool that plots the last photon packet interactions by velocity for each element in supernova ejecta, offering deeper insights into supernova spectra.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: LIV (Last Interaction Velocity) Plot
      keyName: property
    - name: 'og:description'
      value: >-
        Hi, this article highlights the development of the LIV (Last Interaction Velocity) Plot during this summer's GSoC program—a new visualization tool that plots the last photon packet interactions by velocity for each element in supernova ejecta, offering deeper insights into supernova spectra.
      keyName: property
    - name: 'og:image'
      value: ../articles/LIV_ply.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: LIV (Last Interaction Velocity) Plot
    - name: 'twitter:description'
      value: >-
        Hi, this article highlights the development of the LIV (Last Interaction Velocity) Plot during this summer's GSoC program—a new visualization tool that plots the last photon packet interactions by velocity for each element in supernova ejecta, offering deeper insights into supernova spectra.
    - name: 'twitter:image'
      value: ../articles/LIV_ply.png
      relativeUrl: true
layout: post
---

The TARDIS SDEC plot visualizes which atoms photon packets interact with before they escape the ejecta and contribute to the output spectrum's absorption and emission features. However, the SDEC plot does not visualize where these interactions occur within the ejecta. This information can be beneficial to astronomers who want to understand which regions of the ejecta are responsible for important features in the output spectrum.

This project develops the LIV (Last Interaction Velocity) Plot that plots the number of photon packet interactions as a velocity function for each element present in the ejecta. One such example is shown in the plot below.

<img src='\../articles/LIV_mpl.png' alt='Image'>

We can create a highly informative and visually appealing Last Interaction Velocity plot using Matplotlib, If you're using the Last Interaction Velocity plot for exploration, consider creating an interactive version with Plotly. This allows you to zoom, pan, and inspect data values by hovering, resizing the scale, and more conveniently.

<img src='\../articles/plotly-gif.gif' alt='Image'>

The plots have various options providing the users with more control over how your last interaction velocity looks, like, 'species_list', 'nelements', 'packet_wvl_range', 'num_bins', 'log_scale' and many other options.

The detailed report for the GSoC project is available <a href='https://sites.google.com/view/sarthak-gsoc2024/home'>here</a>.


