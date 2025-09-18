# 📦 rsdocx Extractor

DesignSpark Mechanicalファイル（.rsdocx）から3Dジオメトリデータを抽出するWebアプリケーションです。

![rsdocx Converter Application](https://github.com/user-attachments/assets/a1388ff0-927d-4682-900d-98c3ca9859dd)

## 🚀 特徴

### 🔐 プライバシー保護
- **完全なクライアントサイド処理**: ファイルはブラウザ内でのみ処理され、外部サーバーに送信されません
- **データ安全性**: アップロードされたファイルは一切外部に漏れることがありません

### ⚡ 高速処理
- **サーバー通信不要**: ネットワーク遅延なしで即座にファイル処理を実行
- **リアルタイム変換**: ドラッグ&ドロップで即座に変換開始

### 📱 どこでも利用可能
- **インターネット接続不要**: オフライン環境でも動作
- **クロスプラットフォーム**: Windows、Mac、Linuxのブラウザで動作
- **インストール不要**: Webブラウザさえあれば利用可能

## 🛠️ 機能

### 対応ファイル形式
- **入力**: DesignSpark Mechanical ファイル（.rsdocx）
- **出力**: Parasolid 3Dファイル（.x_b）およびその他のジオメトリファイル

### 抽出機能
- rsdocxファイル内の `SpaceClaim/Geometry/` フォルダから3Dジオメトリファイルを自動抽出
- 複数ファイルが含まれている場合は、ZIPアーカイブとして一括ダウンロード
- 単一ファイルの場合は、直接ダウンロード

## 📋 使用方法

1. **ファイル選択**
   - Webアプリケーションを開く
   - rsdocxファイルをドラッグ&ドロップするか、クリックしてファイルを選択

2. **自動処理**
   - アップロード後、自動的にファイル解析が開始
   - 進行状況がプログレスバーで表示

3. **ダウンロード**
   - 抽出完了後、ダウンロードボタンが表示
   - 3Dジオメトリファイル（.x_bなど）をダウンロード

## 🔧 技術仕様

### 使用技術
- **フロントエンド**: HTML5、CSS3、JavaScript（ES6+）
- **ファイル処理**: JSZip ライブラリ
- **動作環境**: モダンWebブラウザ（Chrome、Firefox、Safari、Edge）

### アーキテクチャ
- **完全なクライアントサイド**: サーバーレスアーキテクチャ
- **Progressive Web App**: オフライン対応

## 📁 プロジェクト構成

```
rsdocx_converter/
├── README.md          # このファイル
└── doc/
    └── index.html     # メインのWebアプリケーション
```

## 🚀 セットアップ

### ローカル開発環境

1. リポジトリをクローン:
```bash
git clone https://github.com/mkt-kuno/rsdocx_converter.git
cd rsdocx_converter
```

2. Webサーバーを起動:
```bash
cd doc
python3 -m http.server 8000
```

3. ブラウザでアクセス:
```
http://localhost:8000
```

### デプロイ

静的サイトホスティングサービス（GitHub Pages、Netlify、Vercelなど）にdocフォルダをデプロイするだけで利用可能です。

## 🤝 貢献

プルリクエストや課題報告を歓迎します。

## 📄 ライセンス

このプロジェクトのライセンス情報については、リポジトリ内のLICENSEファイルをご確認ください。

## ⚠️ 注意事項

- DesignSpark Mechanical（.rsdocx）ファイルにのみ対応
- 抽出されるファイルは、元のrsdocxファイル内のSpaceClaim/Geometryフォルダに含まれるもののみ
- ブラウザのJavaScript有効化が必要
