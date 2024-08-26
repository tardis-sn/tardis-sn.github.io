---
title: Enhancing Packet Trackers
excerpt: >-
  Hey there! This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
publishDate: 23th Aug, 2024
thumb_image: ../articles/cover_image.png
seo:
  title: Enhancing Packet Trackers
  description: Hey there! This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Enhancing Packet Trackers
      keyName: property
    - name: 'og:description'
      value: >-
        Hey there! This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
      keyName: property
    - name: 'og:image'
      value: ../articles/cover_image.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Enhancing Packet Trackers
    - name: 'twitter:description'
      value: >-
        Hey there! This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
    - name: 'twitter:image'
      value: ../articles/cover_image.png
      relativeUrl: true
layout: post
---

We have introduced a new RPacketLastInteractionTracker class to keep track of the last interaction of a RPacket.

<img src='\../articles/RPacketLastInteractionTracker.png' alt='Image'>

As a result of the tracker restructuring, the peak memory usage has been reduced from 4 GB to approximately 1 GB.

<strong>Before Restructure</strong>

<img src='\../articles/beforeRestructure.png' alt='Image'>

<strong>After Restructure</strong>

<img src='\../articles/afterRestructure.png' alt='Image'>

Also, we made sure to create lots of tests and benchmarks to ensure that the trackers are working at their best.

The detailed report for the GSoC project is available <a href='https://gist.github.com/Sumit112192/fc0140fa2d11bb903bd2d0e0ce0c8462'>here</a>.


