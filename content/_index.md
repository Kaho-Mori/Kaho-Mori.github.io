---
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      username: me
      text: ''
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: md
      avatar:
        size: medium
        shape: circle
  - block: markdown
    content:
      title: 'My Research'
      subtitle: ''
      text: |-
        I am a Ph.D. student at the Graduate School of Frontier Sciences, The University of Tokyo, and the Atmosphere and Ocean Research Institute. My research focuses on marine microbiology and microbial ecology — particularly how microbial communities in the ocean respond to physical forcing and contribute to biogeochemical cycles.

        Feel free to [reach out](mailto:) for collaboration!
    design:
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Recent Papers
      filters:
        folders:
          - publications
      count: 3
    design:
      view: citation
      columns: '1'
  - block: collection
    id: talks
    content:
      title: Recent Talks
      filters:
        folders:
          - events
      count: 3
    design:
      view: card
      columns: '1'
  - block: collection
    id: news
    content:
      title: Recent Posts
      filters:
        folders:
          - blog
      count: 3
    design:
      view: card
      columns: '1'
---
