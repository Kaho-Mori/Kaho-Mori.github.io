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
        <div class="flex flex-wrap gap-3 mt-6">
          <a href="/uploads/cv_en.pdf" class="inline-flex items-center gap-2 rounded-lg bg-primary-600 px-5 py-2.5 text-sm font-semibold text-white shadow hover:bg-primary-500 transition">
            📄 Download CV (en)
          </a>
          <a href="/uploads/cv_ja.pdf" class="inline-flex items-center gap-2 rounded-lg bg-primary-600 px-5 py-2.5 text-sm font-semibold text-white shadow hover:bg-primary-500 transition">
            📄 Download CV (ja)
          </a>
        </div>
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      background:
        gradient_mesh:
          enable: true
      name:
        size: large
      avatar:
        size: large
        shape: circle
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
