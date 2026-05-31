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

## TODO: Adding Japanese/English Language Switching

> **削除予定メモ** — 対応が完了したらこのセクションを削除する。

### Step 1: `config/_default/languages.yaml` を編集

```yaml
en:
  languageName: English
  weight: 1

ja:
  languageName: 日本語
  weight: 2
```

### Step 2: `config/_default/params.yaml` で言語スイッチャーを有効化

```yaml
# すでに language_switcher: true になっている場合は不要
header:
  navbar:
    language_switcher: true
```

### Step 3: `config/_default/menus.yaml` を言語ごとに分ける

```yaml
# 英語メニュー
main:
  - name: Bio
    url: /
    weight: 10
  # ...

# 日本語メニュー
main.ja:
  - name: プロフィール
    url: /ja/
    weight: 10
  # ...
```

### Step 4: コンテンツを翻訳する（ページ単位で対応可）

翻訳したいページと同じフォルダに `index.ja.md` を追加するだけ。
翻訳がないページは自動的に英語にフォールバックするので、部分対応でも問題なし。

```
content/
└── publications/
    └── sukigara_2025_peps/
        ├── index.md       ← 英語
        └── index.ja.md    ← 日本語（追加）
```

`index.ja.md` のフロントマターは `index.md` と同じ構造で、`abstract` や `summary` などを日本語で書く。

### Step 5: ホームページ・固定ページの翻訳

`content/_index.md` → `content/_index.ja.md` を作成。
`content/experience.md` → `content/experience.ja.md` を作成。

### Step 6: `data/authors/me.yaml` の多言語対応

`data/authors/me.ja.yaml` を作成し、`bio`・`role` などを日本語で記述。

---

## Local Development

```bash
# Install dependencies
pnpm install

# Start dev server (http://localhost:1313)
pnpm dev
```
