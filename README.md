# 株式会社Boxernet コーポレートサイト（Jekyll / GitHub Pages）

株式会社Boxernetのコーポレートサイトのテーマサンプルです。GitHub Pages でそのまま公開できます。

## ディレクトリ構成

```
2026-04-17_Boxernet_GitHubPages/
├── _config.yml              # サイト設定・会社情報（中央管理）
├── _layouts/
│   └── default.html         # 全ページ共通レイアウト
├── assets/
│   └── css/
│       └── style.css        # カスタムCSS（レスポンシブ対応）
├── index.md                 # トップページ
├── company.md               # 会社概要（/company/）
├── business.md              # 事業内容（/business/）
├── contact.md               # お問い合わせ（/contact/）
├── Gemfile                  # Ruby依存関係
└── README.md                # このファイル
```

## 会社情報の一元管理

会社情報は `_config.yml` の `company:` セクションで一元管理しています。変更は1箇所でOKです。

```yaml
company:
  name: 株式会社Boxernet
  founded: 2023年2月7日
  capital: 310万円
  ceo: 高橋 明宏
  address: 東京都豊島区
  patent_number: "第7534835号"
  email: info@boxernet.online
```

各 Markdown ファイルから `{{ site.company.name }}` のように参照できます。

## ローカルでの確認方法

```bash
# Ruby / Bundler がインストール済みの前提
bundle install
bundle exec jekyll serve

# ブラウザで http://localhost:4000 を開く
```

## GitHub Pages での公開手順

1. GitHub に新規リポジトリを作成（例：`boxernet/boxernet.github.io` または任意のリポジトリ）
2. このフォルダの中身をリポジトリにプッシュ
3. リポジトリの `Settings` → `Pages` で `Source` を `Deploy from a branch` → `main` → `/ (root)` に設定
4. 数分待つと `https://<ユーザー名>.github.io/<リポジトリ名>/` で公開

### 独自ドメイン（boxernet.online）を使う場合

1. リポジトリルートに `CNAME` ファイルを作成し、1行目に `boxernet.online` と記載
2. DNS 側で GitHub Pages の IP または `<ユーザー名>.github.io` への CNAME を設定
3. `_config.yml` の `url:` をドメインに合わせて更新

## カスタマイズ

- **カラー変更**: `assets/css/style.css` の `:root` セクションにあるCSS変数を編集
- **ナビゲーション追加**: `_config.yml` の `nav:` にエントリを追加
- **ページ追加**: 新しい `.md` ファイルを作成し、frontmatter に `layout: default` と `permalink:` を記載

## 推奨プラグイン

- `jekyll-seo-tag` — OGP / Twitter Card メタタグの自動生成
- `jekyll-sitemap` — sitemap.xml の自動生成
- `jekyll-feed` — RSSフィードの自動生成

すべて GitHub Pages でサポートされています。
