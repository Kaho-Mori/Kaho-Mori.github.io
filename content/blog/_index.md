---
title: Note
type: landing

sections:
  - block: markdown
    content:
      title: 'Note'
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

  - block: markdown
    content:
      title: '📍 Pinned Post'
      text: |
        {{< pinned-posts >}}
    design:
      columns: '1'

  - block: collection
    content:
      title: 'Post List'
      filters:
        folders:
          - blog
    design:
      view: article-grid
      columns: '2'
---
