---
title: ''
summary: ''
date: 2022-10-24
type: landing

sections:
  - block: resume-biography-3
    content:
      username: me
      text: |
        {{< author-bio >}}
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        image:
          filename: bg_light.jpg
          size: cover
          position: center
      name:
        size: large
      avatar:
        size: large
        shape: square
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
    id: news
    content:
      title: Recent Posts
      filters:
        folders:
          - blog
      count: 3
    design:
      view: article-grid
      columns: '2'
---
