---
title: Enhancing Packet Trackers
excerpt: >-
  This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
publishDate: 2024-08-23
thumb_image: ../articles/cover_image_sharpened.png
seo:
  title: Enhancing Packet Trackers
  description: This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
  extra:
    - name: 'og:type'
      value: website
      keyName: property
    - name: 'og:title'
      value: Enhancing Packet Trackers
      keyName: property
    - name: 'og:description'
      value: >-
        This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
      keyName: property
    - name: 'og:image'
      value: ../articles/cover_image_sharpened.png
      keyName: property
      relativeUrl: true
    - name: 'twitter:card'
      value: summary_large_image
    - name: 'twitter:title'
      value: Enhancing Packet Trackers
    - name: 'twitter:description'
      value: >-
        This article covers all the cool stuff we've been up to this summer for the GSoC project related to packet trackers.
    - name: 'twitter:image'
      value: ../articles/cover_image_sharpened.png
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

We also added detailed boundary interaction to the RPacketTracker, the structure of which looks like

<img src='\../articles/boundary_interaction.png' alt='Image'>

`event_id` is the interaction number, `current_shell_id` is the previous boundary, and `next_shell_id` is the shell id to which the packet moved

We also researched a lot about Numba. Some of the things included using dynamic variables inside Numba using approaches like overload, branch pruning, etc., if you are interested about it, here are some <a href='https://gist.github.com/Sumit112192/6ddf8cb7be016caba1ce98feca95815d'>toy code.</a>

Also, we made sure to create lots of tests and benchmarks to ensure that the trackers are working at their best.

The detailed report for the GSoC project is available <a href='https://gist.github.com/Sumit112192/fc0140fa2d11bb903bd2d0e0ce0c8462'>here</a>.


