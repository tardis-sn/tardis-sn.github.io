---
title: Home
sections:
  - section_id: hero
    type: section_hero
    image_alt: App preview
    title: TARDIS Project
    background_image: images/hubblecast.png
    image_alt: Exploding supernova
    content: >-
      An open-science software to simulate and analyse supernovae and other transients
    actions:
      - label: Learn More
        url: /#features
        style: primary
  - section_id: features
    type: section_features
    background: white
    title: TARDIS at a Glance
    subtitle: >-
      TARDIS packages provide several tools for physics calculation and visualization to make your supernova research easier. 
    features:
      - title: Modeling supernovae made easy
        image: images/config_and_modeling.png
        image_alt: App preview on a phone and tablet
        content: >-
          With <a href="https://tardis-sn.github.io/tardis" target="_blank" rel="noopener nofollow">tardis</a> (our Monte Carlo radiative-transfer code), you can control simulation parameters and access physical properties of the model in an intuitive way.
        actions:
          - label: Learn More
            url: https://tardis-sn.github.io/tardis/quickstart.html
            style: secondary
            has_icon: true
            icon: arrow-right
            icon_position: right
      - title: Visualise the model in multiple ways 
        image: images/visualization_sdec_plot.png
        image_alt: App users welcoming a new member
        content: >-
          After simulation, use our variety of tools to generate diagnostic visualizations and Jupyter widgets (GUI) to interactively explore the data.
        actions:
          - label: Learn More
            url: https://tardis-sn.github.io/tardis/io/visualization/index.html
            style: secondary
            has_icon: true
            icon: arrow-right
            icon_position: right
      - title: Atomic data ready to use
        image: images/carsus_io_diagram.png
        image_alt: App user profile preview
        content: >-
          Our <a href="https://tardis-sn.github.io/carsus" target="_blank" rel="noopener nofollow">carsus</a> package can read atomic data from a variety of sources and output them to file formats readable by tardis and other radiative transfer codes.
        actions:
          - label: Learn More
            url: https://tardis-sn.github.io/carsus/
            style: secondary
            has_icon: true
            icon: arrow-right
            icon_position: right
  # - section_id: reviews
  #   type: section_reviews
  #   background: white
  #   title: Testimonials
  #   subtitle: >-
  #     Aliquam malesuada ligula eget est fringilla blandit. Integer finibus
  #     semper libero id sodales.
  #   reviews:
  #     - author: Eric Widget
  #       avatar: images/review1.jpg
  #       avatar_alt: Eric Widget's photo
  #       content: >-
  #         Vestibulum a nunc ut eros condimentum posuere. Nullam dapibus quis
  #         nunc non interdum. Pellentesque tortor ligula, gravida ac commodo eu.
  #     - author: Parsley Montana
  #       avatar: images/review2.jpg
  #       avatar_alt: Parsley Montana's photo
  #       content: >-
  #         Sed laoreet magna commodo libero euismod sodales. Nunc ac libero
  #         convallis, interdum ligula vel, pretium diam. Integer commodo sem at
  #         dui sollicitudin, vel posuere justo laoreet.
  #     - author: Jonquil Von Haggerston
  #       avatar: images/review3.jpg
  #       avatar_alt: Jonquil Von Haggerston's photo
  #       content: >-
  #         Integer consectetur purus neque, ac porttitor enim convallis vitae.
  #         Interdum et malesuada fames ac ante ipsum primis in faucibus.
  - section_id: call-to-action
    type: section_cta
    title: Try out all of this online!
    subtitle: Launch an interactive version of our quickstart Jupyter notebook
    actions:
      - label: Get Started
        url: https://mybinder.org/v2/gh/tardis-sn/tardis/HEAD?filepath=docs/quickstart.ipynb
        style: primary
  - section_id: twitter_widget
    type: twitter_widget
    background: white
    title: Latest Posts
seo:
  title: TARDIS-SN
  description: An open-science software to simulate and analyse supernovae and other transients
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: TARDIS-SN
      keyName: property
    - name: 'og:description'
      value: An open-science software to simulate and analyse supernovae and other transients
      keyName: property
    - name: 'og:image'
      value: images/hero.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: TARDIS-SN
    - name: 'twitter:description'
      value: An open-science software to simulate and analyse supernovae and other transients
    - name: 'twitter:image'
      value: images/hero.png
      relativeUrl: true
layout: landing
---
