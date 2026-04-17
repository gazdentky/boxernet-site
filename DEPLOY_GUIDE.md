# Boxernet コーポレートサイト 公開手順書

GitHub Pages を使って `boxernet.online` で正式公開するまでの手順です。

---

## 目次

1. 前提の確認
2. 事前準備（GitHubアカウント・Git）
3. GitHub にリポジトリを作成
4. サイトファイルをアップロード
5. GitHub Pages を有効化
6. 独自ドメイン `boxernet.online` を設定
7. DNS の設定（ムームードメイン／お名前.com など）
8. HTTPS の有効化
9. サイトの更新方法
10. トラブルシューティング

---

## 1. 前提の確認

公開前に、以下を準備します。

| 項目 | 内容 |
|------|------|
| サイトファイル | `2026-04-17_Boxernet_GitHubPages/` フォルダ一式 |
| GitHubアカウント | 無料プランでOK |
| 独自ドメイン | `boxernet.online`（取得済み前提） |
| DNSアクセス権 | ドメイン取得元の管理画面にログインできること |

---

## 2. 事前準備

### 2-1. GitHubアカウント作成

すでにアカウントがある場合はスキップ。

1. ブラウザで https://github.com/signup にアクセス
2. メールアドレス・パスワード・ユーザー名を入力（例：`boxernet`）
3. メール認証を完了

### 2-2. Git のインストール確認

Mac で以下のコマンドを実行して Git がインストールされているか確認します。

```bash
git --version
```

未インストールの場合は、ターミナルで以下を実行するか、https://git-scm.com/download/mac からインストーラをダウンロード。

```bash
# Homebrew がある場合
brew install git
```

### 2-3. GitHub との認証設定（初回のみ）

ターミナルで以下を実行し、コミット時の名前とメールを設定。

```bash
git config --global user.name "あなたの名前"
git config --global user.email "あなたのメールアドレス"
```

GitHub への認証は「Personal Access Token」または SSH キーが必要です。最も簡単なのは **GitHub CLI** を使う方法です。

```bash
# GitHub CLI のインストール
brew install gh

# ログイン（ブラウザが開くので画面の指示に従う）
gh auth login
```

`HTTPS` を選び、ブラウザでの認証を選択すると自動で完了します。

---

## 3. GitHub にリポジトリを作成

### 方法A: ブラウザで作成（推奨・簡単）

1. https://github.com/new にアクセス
2. 以下を入力：
   - **Repository name**: `boxernet-site`（任意の名前でOK）
   - **Visibility**: `Public`（GitHub Pages の無料枠は Public が条件）
   - **Initialize this repository**: チェック**しない**（ローカルから上げるため）
3. `Create repository` ボタンを押す
4. 作成されたリポジトリの URL をメモ（例：`https://github.com/boxernet/boxernet-site`）

### 方法B: ターミナルで作成（gh CLI使用）

```bash
gh repo create boxernet-site --public --description "株式会社Boxernet コーポレートサイト"
```

---

## 4. サイトファイルをアップロード

### 4-1. 公開用フォルダを準備

Finder で以下のフォルダを **デスクトップなどの短いパス** にコピーします（日本語パスのままだと Git で問題が出ることがあるため）。

```
元: マイドライブ/Claude Code 出力/03_事業計画・提案書/2026-04-17_Boxernet_GitHubPages/
先: ~/Desktop/boxernet-site/
```

### 4-2. 不要ファイルの除去

コピー先フォルダ内で、以下を削除します（公開不要）。

- `_preview/` フォルダ
- `.claude/` フォルダ（もしあれば）
- `Gemfile.production`（ローカル開発時に一時リネームしたもの → 元の `Gemfile` に戻す）

```bash
cd ~/Desktop/boxernet-site
rm -rf _preview .claude
# Gemfile.production があれば Gemfile に戻す
[ -f Gemfile.production ] && mv Gemfile.production Gemfile
```

### 4-3. `.gitignore` を作成

ビルド成果物やログは Git 管理から除外します。

```bash
cat > .gitignore <<'EOF'
_site/
.sass-cache/
.jekyll-cache/
.jekyll-metadata
vendor/
.DS_Store
Gemfile.lock
EOF
```

### 4-4. Git 初期化 → GitHubへプッシュ

```bash
cd ~/Desktop/boxernet-site

git init
git add .
git commit -m "Initial commit: Boxernet corporate site"

# GitHub のリポジトリURLに合わせて変更
git branch -M main
git remote add origin https://github.com/boxernet/boxernet-site.git
git push -u origin main
```

プッシュ完了後、GitHub のリポジトリページをブラウザでリロードすると全ファイルがアップされています。

---

## 5. GitHub Pages を有効化

1. GitHub のリポジトリページを開く
2. 上部タブの `Settings` をクリック
3. 左メニューの `Pages` をクリック
4. `Build and deployment` セクションで以下を設定：
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / `/ (root)` → `Save`
5. 数分待つと、ページ上部に緑色で以下のように表示されます：
   ```
   Your site is live at https://<ユーザー名>.github.io/boxernet-site/
   ```
6. このURLをクリックしてサイトが表示されれば成功

**この時点では**、`https://boxernet.github.io/boxernet-site/` のような GitHub サブドメインで公開されます。

---

## 6. 独自ドメイン `boxernet.online` を設定

### 6-1. リポジトリに CNAME ファイルを追加

ローカル（`~/Desktop/boxernet-site/`）で以下を実行：

```bash
echo "boxernet.online" > CNAME
git add CNAME
git commit -m "Add custom domain"
git push
```

または GitHub の Pages 設定画面で `Custom domain` に `boxernet.online` と入力して `Save` を押すと、自動で `CNAME` ファイルが作成されます（推奨）。

### 6-2. `_config.yml` の `url:` を本番ドメインに変更

```yaml
url: "https://boxernet.online"
baseurl: ""
```

変更後、同じ手順でコミット・プッシュ。

---

## 7. DNS の設定

ドメインを取得したサービス（お名前.com、ムームードメイン、Google Domains、Cloudflare 等）の管理画面にログインし、以下のレコードを設定します。

### 7-1. Apex ドメイン（`boxernet.online`）用

**Aレコード** を 4つ作成し、以下の GitHub の IP アドレスを登録します。

| タイプ | ホスト名 | 値 |
|--------|---------|-----|
| A | `@`（または空欄） | `185.199.108.153` |
| A | `@` | `185.199.109.153` |
| A | `@` | `185.199.110.153` |
| A | `@` | `185.199.111.153` |

### 7-2. `www` サブドメイン用（任意だが推奨）

| タイプ | ホスト名 | 値 |
|--------|---------|-----|
| CNAME | `www` | `<ユーザー名>.github.io`（例：`boxernet.github.io`） |

### 7-3. 反映確認

DNS の反映には **数分〜最大48時間** かかる場合があります。以下で確認できます。

```bash
dig boxernet.online +short
# → 185.199.108.153 など4つのIPが返れば成功

dig www.boxernet.online +short
# → boxernet.github.io. に続くIPが返れば成功
```

---

## 8. HTTPS の有効化

1. GitHub のリポジトリ `Settings` → `Pages` に戻る
2. `Custom domain` 欄に `boxernet.online` が入っていることを確認
3. **DNSが反映されると** 下に `✓ DNS check successful` と表示される
4. その下の `Enforce HTTPS` のチェックボックスを **ON** にする
   - 反映まで数分〜数時間かかる場合があります
   - チェックが押せない場合は DNS の反映待ち

これで `https://boxernet.online` で SSL 証明書付きで公開されます。

---

## 9. サイトの更新方法

ページを修正した後は、以下の3コマンドで公開されます。

```bash
cd ~/Desktop/boxernet-site

# 変更内容を確認
git status

# 変更をステージング
git add .

# コミット（修正内容を記述）
git commit -m "会社概要ページの住所を更新"

# GitHub にプッシュ
git push
```

プッシュ後、GitHub Actions が自動でビルドし、**数分で本番サイトに反映**されます。

進捗はリポジトリの `Actions` タブで確認できます。

### ローカルでの事前確認

プッシュ前にローカルで確認したい場合：

```bash
cd ~/Desktop/boxernet-site
jekyll serve
# → http://localhost:4000 で確認
```

---

## 10. トラブルシューティング

### ❌ サイトが404になる

**原因**: GitHub Pages のビルドが完了していない、または失敗している

**対処**:
1. リポジトリの `Actions` タブを確認
2. 赤いバツマークがあればクリックしてエラー内容を確認
3. ビルドエラーは多くの場合、YAML の書式間違い（`_config.yml`）

### ❌ CSS が適用されない

**原因**: `_config.yml` の `baseurl` と実際のURLが不一致

**対処**:
- `<ユーザー名>.github.io/boxernet-site/` で公開 → `baseurl: "/boxernet-site"`
- `boxernet.online` で公開 → `baseurl: ""`

### ❌ 独自ドメインの DNS check に失敗する

**原因**: DNS の反映待ち、または A レコードの値が間違っている

**対処**:
- `dig boxernet.online +short` で4つのGitHub IPが返るか確認
- ドメイン管理画面で A レコードのホスト名が `@` または空欄になっているか確認
- 反映まで最大48時間かかる場合あり

### ❌ HTTPS の証明書エラー

**原因**: 証明書発行が未完了

**対処**: 初回は数時間かかることがあります。24時間待ってから再度確認。それでも直らない場合は `Custom domain` を一度削除 → 再登録で再発行されます。

### ❌ 日本語が文字化けする

**原因**: ファイルのエンコーディングが UTF-8 でない

**対処**: すべての `.md` ファイルが UTF-8 で保存されているか確認

---

## 参考リンク

- [GitHub Pages 公式ドキュメント](https://docs.github.com/pages)
- [Jekyll 公式ドキュメント](https://jekyllrb.com/)
- [GitHub Pages で独自ドメインを使う](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site)

---

## 公開後のチェックリスト

- [ ] `https://boxernet.online` でトップページが表示される
- [ ] 全4ページ（HOME、事業内容、会社概要、お問い合わせ）にアクセスできる
- [ ] ヘッダー・フッターのリンクが正常に動作する
- [ ] スマートフォンで表示が崩れない
- [ ] `info@boxernet.online` のメールリンクが動作する
- [ ] HTTPS（鍵マーク）が有効になっている
- [ ] SEO検索結果に表示される（1週間〜数週間かかる）

---

以上で公開完了です。お疲れさまでした。
