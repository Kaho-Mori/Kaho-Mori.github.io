# Kaho Mori — Personal Academic Website

Source code for **[Kaho-Mori.github.io](https://Kaho-Mori.github.io)**, the personal academic website of 森 香穂 (Kaho Mori), Ph.D. student at the Graduate School of Frontier Sciences, The University of Tokyo / Atmosphere and Ocean Research Institute.

## Site Structure

| Section | Directory | Description |
| :--- | :--- | :--- |
| Bio (homepage) | `content/_index.md` | Profile, recent papers/presentations/posts |
| Publications | `content/publications/` | Peer-reviewed papers and thesis |
| Presentations | `content/presentations/` | Conference talks and posters |
| CV | `content/cv.md` | Education, work, awards, certifications, cruises |
| Blog | `content/blog/` | Fieldwork notes and research updates |

## Adding Content

**New publication** — copy `content/publications/sukigara_2025_peps/` and edit `index.md`.

**New presentation** — copy any folder under `content/presentations/` and edit `index.md`.  
Directory naming convention: `20xx_学会略称+回数_場所`

**New blog post** — create a new folder under `content/blog/` with an `index.md`.

- `date`: 論文・発表の日付。一覧での並び順やページ上の表示日付に使われる。
- `publishDate`: サイト上でこのページを公開する日。この日付より前だと Hugo がビルドしてもページが生成されない（予約公開機能）。

## Profile Data — どこを編集すればどこに反映されるか

プロフィールデータは **`data/authors/me.yaml` を編集する**のが基本。

| 変更したい内容 | 編集するファイル | 反映される場所 |
| :--- | :--- | :--- |
| 名前・役職・所属 | `data/authors/me.yaml` → `name` / `role` / `affiliations` | Bio（トップ）|
| プロフィール文 | `data/authors/me.yaml` → `bio` | Bio（トップ）|
| アイコン写真 | `assets/media/authors/me.jpg` を差し替え | Bio（トップ）|
| ソーシャルリンク | `data/authors/me.yaml` → `links` | Bio（トップ）|
| 研究興味 | `data/authors/me.yaml` → `interests` | Bio（トップ）|
| 学歴 | `data/authors/me.yaml` → `education` | Bio（トップ）・CV |
| 職歴 | `data/authors/me.yaml` → `work` | CV |
| 受賞・資金 | `data/authors/me.yaml` → `awards` | CV |

> `content/authors/me/_index.md` は著者システムの内部設定のみ（編集不要）。

## 見た目のカスタマイズ — どこを触ると何が変わるか

### `config/_default/params.yaml` — メインの設定ファイル

| 変更したい内容 | キー | 値の例 |
| :--- | :--- | :--- |
| サイト名（ナビバー・タイトル） | `identity.name` | `"Kaho Mori"` |
| サイト説明文（SEO用） | `identity.description` | 任意のテキスト |
| Twitter/X ハンドル（OGP用） | `identity.social.twitter` | `"yourhandle"` |
| テーマカラー | `theme.colors.primary` | `"indigo"` / `"#6366f1"` |
| ライト/ダーク/システム | `theme.mode` | `light` / `dark` / `system` |
| フォント | `typography.pack` | `"academic"` / `"minimal"` |
| 角丸の強さ | `layout.radius` | `none` / `sm` / `md` / `lg` / `full` |
| 余白の広さ | `layout.spacing` | `compact` / `comfortable` / `spacious` |
| アバターの形 | `layout.avatar_shape` | `circle` / `square` / `rounded` |
| ナビバーのスタイル | `header.style` | `navbar` / `navbar-simple` / `minimal` |
| ナビバーの位置 | `header.align` | `left` / `center` / `right` |
| 検索ボタン表示 | `header.search` | `true` / `false` |
| ダーク/ライト切替ボタン | `header.theme_toggle` | `true` / `false` |
| フッタースタイル | `footer.style` | `minimal` / `columns` / `centered` |
| 日付フォーマット | `locale.date_format` | `"Jan 2, 2006"` |
| Google Analytics | `analytics.google.measurement_id` | `"G-XXXXXXXXXX"` |

### `config/_default/menus.yaml` — ナビゲーションメニュー

ナビバーに表示するリンクの名前・URL・順序を管理。  
`weight` の数値が小さいほど左側に表示される。

### `assets/css/custom.css` — 細かいスタイル調整

HugoBlox のデフォルトで対応できない見た目の変更を直接 CSS で書く場所。  
コメントに各ルールの意図を記載している。

### `data/themes/` — テーマカラーのカスタム定義（上級者向け）

独自のカラーパレットを作りたい場合、このディレクトリに YAML ファイルを作成し  
`params.yaml` の `theme.pack` でその名前を指定する。

### `data/fonts/` — フォントのカスタム定義（上級者向け）

独自のフォント設定を作りたい場合、このディレクトリに YAML ファイルを作成し  
`params.yaml` の `typography.pack` でその名前を指定する。

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
`content/cv.md` → `content/cv.ja.md` を作成。

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
