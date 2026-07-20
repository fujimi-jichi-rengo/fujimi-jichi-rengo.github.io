# ふじみ地区自治会等連合会 - 公式ウェブサイト

調布市北部地域（深大寺東町、北町）における自治会等連合会の公式ウェブサイトです。

## 📍 概要

ふじみ地区自治会等連合会は、地区内の自治会や市民団体が連携し、以下のテーマで社会貢献活動を行っています：

- 🌱 **環境保全** - 地域の環境整備と美化活動
- 🛡️ **安全・防犯** - 防犯パトロールと安全啓発
- ❤️ **福祉・交流** - 高齢者支援と世代間交流

## 🌐 ウェブサイト

- **公開URL**: https://fujimijichirengo-crypto.github.io/news
- **ホスティング**: GitHub Pages
- **構成**: 静的HTML + CSS + JavaScript

## 📁 ディレクトリ構造

```
.
├── dist/                      # 公開用ディレクトリ（GitHub Pages）
│   ├── index.html            # ホームページ
│   ├── about.html            # 当会について
│   ├── activities.html       # 活動実績・成果
│   ├── newsletter.html       # 連合会会報
│   ├── lectures.html         # 連合会講座
│   ├── contact.html          # お問い合わせ
│   └── src/
│       ├── css/style.css     # メインスタイル
│       └── js/main.js        # メインJavaScript
├── pages/
│   ├── raw-html/             # 元のJimdoサイトのHTML
│   └── analysis.json         # コンテンツ分析結果
├── src/                       # ソースファイル
│   ├── css/style.css
│   ├── js/main.js
│   └── base.html             # テンプレート
├── _config.yml               # Jekyll設定
└── README.md                 # このファイル
```

## 🎨 デザイン

### カラースキーム

- **プライマリ**: #2c5f8d（深青）
- **セカンダリ**: #4db8a8（ティール）
- **アクセント**: #f39c12（オレンジ）

### レスポンシブ対応

- デスクトップ（1200px以上）
- タブレット（768px - 1199px）
- モバイル（767px以下）

## 🚀 ローカル開発

### セットアップ

```bash
# リポジトリのクローン
git clone https://github.com/fujimijichirengo-crypto/news.git
cd news

# ローカルサーバーの起動（Python）
python3 -m http.server 8000 --directory dist
```

ブラウザで `http://localhost:8000` を開くと確認できます。

### ファイル編集

- **HTMLページ**: `dist/*.html`を編集
- **CSS**: `dist/src/css/style.css`を編集
- **JavaScript**: `dist/src/js/main.js`を編集

編集後、ブラウザで変更を確認できます。

## 📝 コンテンツ管理

### ページの追加

1. `dist/`に新しいHTMLファイルを作成
2. 既存ページと同じ構造（header, footer）を使用
3. ナビゲーションにリンクを追加

### テンプレート構造

```html
<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="...">
    <title>ページタイトル - ふじみ地区自治会等連合会</title>
    <link rel="stylesheet" href="src/css/style.css">
</head>
<body>
    <!-- ヘッダー（全ページ共通） -->
    <header>...</header>
    
    <!-- メインコンテンツ -->
    <main>
        <div class="container">
            <!-- ページ固有のコンテンツ -->
        </div>
    </main>
    
    <!-- フッター（全ページ共通） -->
    <footer>...</footer>
    
    <script src="src/js/main.js"></script>
</body>
</html>
```

## 🔧 更新方法

1. `dist/`内のファイルを編集
2. `git`でコミット
   ```bash
   git add .
   git commit -m "ページ更新: ..."
   git push origin main
   ```
3. GitHub Actionsが自動でデプロイ

## 📞 サポート

質問や要望は、ウェブサイトの「お問い合わせ」ページからお気軽にご連絡ください。

## 📄 ライセンス

© 2024 ふじみ地区自治会等連合会. All rights reserved.

---

**最終更新**: 2024年7月
