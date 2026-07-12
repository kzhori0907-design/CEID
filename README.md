# 産官学イノベーション共創センター Webサイト

静的サイト（HTML / CSS / JavaScript のみ）です。サーバー側の処理は不要で、GitHub Pages でそのまま公開できます。

## ファイル構成

```
├── index.html              トップ（センター概要・事業紹介・部門・お知らせ・お問い合わせ）
├── bridge.html             BRIDGE（橋渡しプログラム）
├── dept-ai.html            教育AI・データサイエンス共創推進部門
├── dept-science.html       科学・次世代教育研究部門
├── dept-facilitation.html  産官学共創ファシリテーション部門
├── results.html            共同研究・連携実績
├── sitemap.html            サイトマップ
├── en/
│   ├── index.html          英語トップ
│   └── bridge.html         英語BRIDGE
└── assets/
    ├── style.css           共通スタイル
    └── script.js           モバイルナビ・スクロール表示
```

## GitHub Pages での公開手順

1. GitHubで新しいリポジトリを作成（例: `center-website`）
2. このフォルダの中身をすべてリポジトリのルートにアップロード
   - Web画面から: リポジトリの「Add file → Upload files」でドラッグ&ドロップ
   - コマンドから:
     ```
     git init
     git add .
     git commit -m "初回公開"
     git branch -M main
     git remote add origin https://github.com/ユーザー名/center-website.git
     git push -u origin main
     ```
3. リポジトリの **Settings → Pages** を開く
4. 「Source」を **Deploy from a branch**、Branch を **main / (root)** にして Save
5. 数分後に `https://ユーザー名.github.io/center-website/` で公開されます

## 公開前に差し替えが必要な箇所（`TODO` で検索できます）

- お問い合わせ先（メールアドレス・電話番号・住所）
- 各部門の「主な業務」「スタッフ」情報
- BRIDGEのプロジェクト概要・実施内容・メンバー
- 共同研究・連携実績の表データ
- 外部リンク（みらい教育共創館、年報PDF、高度理系教員養成プログラム、eRA、大学発ベンチャー、共同研究制度等、旧センター）
- お知らせの記事

## 運用（更新方法）

- **お知らせの追加**: `index.html` の `<ul class="news-list">` 内に `<li>` を1行コピーして書き換え
- **部門ページの更新**: 各 `dept-*.html` を編集（担当: 各部門長）
- **BRIDGEの更新**: `bridge.html` を編集
- GitHubにpush（またはWeb画面で編集・Commit）すると自動で反映されます

## 確認事項への対応

- ✅ スマホ閲覧対応（画面幅に応じてレイアウトが自動調整）
- ✅ アクセシビリティ対応（スキップリンク、キーボードフォーカス表示、見出し構造、reduced-motion対応、色コントラスト配慮）
- ✅ PC画面の初回表示で3部門のカードまで表示（ヒーローをコンパクトに設計）
- ✅ 静的サイト（HTML/CSS/JSのみ、CMS不要）
