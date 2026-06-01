---
title: Blog
type: landing

sections:
  - block: markdown
    content:
      title: 'Blog'
      text: ''
    design:
      columns: '1'

  - block: markdown
    content:
      title: ''
      text: |
        {{< tag-cloud >}}
    design:
      columns: '1'

  - block: collection
    content:
      title: ''
      filters:
        folders:
          - blog
    design:
      view: article-grid
      columns: '2'
---
