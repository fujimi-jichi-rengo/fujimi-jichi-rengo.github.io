# GitHub Pages デプロイメント手順

## 前提条件

- このリポジトリは `fujimijichirengo-crypto/news` です
- `main` ブランチに変更がプッシュされています

## デプロイ方法

### ステップ 1: GitHub リポジトリ設定

1. GitHub で https://github.com/fujimijichirengo-crypto/news を開く
2. **Settings** → **Pages** に移動
3. 以下のように設定：
   - **Source**: Deploy from a branch
   - **Branch**: `main` / `/ (root)`
   - または **GitHub Actions** を使用（自動デプロイの場合）

### ステップ 2: サイトの確認

デプロイ後、以下のURLでサイトが公開されます：

```
https://fujimi-jichi-rengo.github.io/
```

### ステップ 3: ローカルテスト（オプション）

デプロイ前にローカルで確認する場合：

```bash
cd dist
python3 -m http.server 8000
```

ブラウザで http://localhost:8000 を開きます。

## 更新手順

ページを更新する場合：

1. `dist/` 内のHTMLファイルを編集
2. 確認用に `python3 -m http.server 8000` で確認
3. `git add`, `git commit`, `git push` で変更を反映

```bash
git add dist/
git commit -m "update: 〇〇ページを更新"
git push origin main
```

4. 数分後、サイトが更新されます

## トラブルシューティング

### サイトが公開されない

- GitHub Pages がリポジトリ設定で有効になっているか確認
- `dist/` ディレクトリが正しく配置されているか確認
- キャッシュをクリアしてブラウザをリロード（Ctrl+Shift+R）

### スタイルが反映されない

- CSSパスが正しいか確認：`src/css/style.css`
- ブラウザキャッシュをクリア

## GitHub Actions による自動デプロイ（推奨）

以下のワークフローを `.github/workflows/pages.yml` に追加すると、
`main` ブランチへのプッシュ時に自動でデプロイされます：

```yaml
name: Deploy to GitHub Pages

on:
  push:
    branches: [main]

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Deploy to GitHub Pages
        uses: actions/upload-artifact@v3
        with:
          name: github-pages
          path: dist/
```

---

**サイトURL**: https://fujimi-jichi-rengo.github.io/
