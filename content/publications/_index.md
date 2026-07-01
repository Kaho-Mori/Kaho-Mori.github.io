---
title: Publications
cms_exclude: true
type: landing

sections:
  - block: markdown
    content:
      title: 'Publications'
      text: ''
    design:
      columns: '1'

  - block: markdown
    content:
      title: ''
      text: |
        <div class="text-center">
        <a href="#papers">Peer-Reviewed Articles</a> · <a href="#preprints">Preprints</a> · <a href="#other">Other Publications</a>
        </div>
    design:
      columns: '1'

  - block: collection
    id: papers
    content:
      title: Peer-Reviewed Articles
      filters:
        folders:
          - publications
        publication_type: article-journal
    design:
      view: article-grid
      columns: '2'

  - block: collection
    id: preprints
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
    id: other
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
