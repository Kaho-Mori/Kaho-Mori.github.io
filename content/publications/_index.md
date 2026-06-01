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
      view: publication-grid
      columns: '2'

  - block: collection
    content:
      title: Preprints
      filters:
        folders:
          - publications
        publication_type: preprint
    design:
      view: publication-grid
      columns: '1'

  - block: collection
    content:
      title: Other Publications
      filters:
        folders:
          - publications
        publication_type: other
    design:
      view: publication-grid
      columns: '2'
---
