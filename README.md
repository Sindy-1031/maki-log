# MAKI-LOG — 薪シェアアプリ PWA

**キャンパー同士で薪情報をシェアするフィールドアプリ**

---

## 📁 ファイル構成

```
maki-log-pwa/
├── index.html        ← アプリ本体（全機能入り）
├── manifest.json     ← PWA設定
├── sw.js             ← Service Worker（オフライン対応）
├── vercel.json       ← Vercel デプロイ設定
├── assets/
│   └── icon.png      ← ★ ロゴ画像をここに配置してください
└── README.md
```

---

## 🚀 Vercel デプロイ手順

### 方法 A: Vercel CLI（推奨）

```bash
# 1. Vercel CLI インストール
npm i -g vercel

# 2. ロゴ配置
cp /path/to/your/logo.png assets/icon.png

# 3. デプロイ
cd maki-log-pwa
vercel

# 初回は対話式で設定。2回目以降は↓
vercel --prod
```

### 方法 B: GitHub + Vercel（ゼロクリック）

1. このフォルダを GitHub リポジトリにプッシュ
2. https://vercel.com → 「Add New Project」
3. リポジトリを選択 → **Framework Preset: Other**
4. **Root Directory: `maki-log-pwa`**
5. 「Deploy」→ 完了！

### 方法 C: Vercel ダッシュボードからドラッグ&ドロップ

1. https://vercel.com にログイン
2. `maki-log-pwa` フォルダをドラッグ&ドロップ

---

## 📲 PWA ホーム画面追加の手順

### iOS (Safari)
1. Safari でアプリURLを開く
2. 下部の「共有」ボタン →「ホーム画面に追加」

### Android (Chrome)
1. Chromeで開くと自動でインストールバナーが表示
2. または: メニュー → 「アプリをインストール」

---

## 🗺️ 地図について

- **Leaflet + OpenStreetMap** を使用（**APIキー不要・完全無料**）
- GPSは `navigator.geolocation` で取得（ブラウザの許可が必要）
- オフライン時はキャッシュされた地図タイルを使用

---

## ⚙️ 機能一覧

| 機能 | 説明 |
|------|------|
| 🗺 マップ | Leaflet地図＋薪スポットピン＋詳細カード |
| 📍 GPS | ブラウザGeolocation API で現在地取得 |
| ✏️ 投稿 | 薪スポット情報の登録（地図にリアルタイム反映） |
| 🏕 レスキュー | RESCUE/GIVEバッジ付き掲示板＋返信機能 |
| 📲 PWA | ホーム画面追加・オフライン対応 |

---

## 🎨 デザインコンセプト

**高級ミリタリーギアカタログ**
- 深チャコール (#0F0F0D) × オリーブドラブ (#4B5320) × 真鍮ゴールド (#C5A059)
- Courier Prime (MONO) フォントによる無骨な印象
- スタガーアニメーション・スライドアップカード

---

Made with 🔥 by MAKI-LOG Team
