# Kaho Mori — Personal Academic Website

Source code for **[Kaho-Mori.github.io](https://Kaho-Mori.github.io)**, the personal academic website of 森 香穂 (Kaho Mori), Ph.D. student at the Graduate School of Frontier Sciences, The University of Tokyo / Atmosphere and Ocean Research Institute.

## Site Structure

| Section | Directory | Description |
| :--- | :--- | :--- |
| Bio (homepage) | `content/_index.md` | Profile, recent papers/presentations/posts |
| Publications | `content/publications/` | Peer-reviewed papers and thesis |
| Presentations | `content/presentations/` | Conference talks and posters |
| Experience | `content/experience.md` | Education and employment history |
| Funding | `content/fund/` | Awards and research funding |
| Blog | `content/blog/` | Fieldwork notes and research updates |

## Adding Content

**New publication** — copy `content/publications/sukigara_2025_peps/` and edit `index.md`.

**New presentation** — copy `content/presentations/JSME_2025_tokyo/` and edit `index.md`.

**New blog post** — create a new folder under `content/blog/` with an `index.md`.

**Profile / CV data** — edit `data/authors/me.yaml` (structured fields) and `content/authors/me/_index.md` (detailed CV).

## Built With

This site is built with [Hugo](https://gohugo.io/) using the [HugoBlox Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) template and deployed via GitHub Pages.

- Template: [HugoBlox Academic CV](https://github.com/HugoBlox/hugo-theme-academic-cv) (MIT License)
- Theme engine: [HugoBlox Kit](https://github.com/HugoBlox/kit)
- HugoBlox homepage: [HugoBlox](https://hugoblox.com/)

## Local Development

```bash
# Install dependencies
pnpm install

# Start dev server (http://localhost:1313)
pnpm dev
```
