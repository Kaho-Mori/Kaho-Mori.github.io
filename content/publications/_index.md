---
title: Publications
cms_exclude: true
type: landing

sections:
  - block: collection
    content:
      title: Publications
      filters:
        folders:
          - publications
        publication_type: article-journal
    design:
      view: article-grid
      columns: '2'

  - block: collection
    content:
      title: Preprints
      filters:
        folders:
          - publications
        publication_type: preprint
    design:
      view: article-grid
      columns: '2'

  - block: collection
    content:
      title: Other Publications
      filters:
        folders:
          - publications
        publication_type: other
    design:
      view: article-grid
      columns: '2'
---
