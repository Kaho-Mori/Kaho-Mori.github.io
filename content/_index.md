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
      button:
        text: 'CV (English)'
        url: uploads/cv_en.pdf
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
        size: large
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
      count: 5
    design:
      view: citation
      columns: '1'
  - block: presentations-table
    id: talks
    content:
      title: 'Upcoming Presentations'
      section: upcoming
  - block: collection
    id: news
    content:
      title: Recent Posts
      filters:
        folders:
          - blog
      count: 5
    design:
      view: compact
      columns: '1'
---
