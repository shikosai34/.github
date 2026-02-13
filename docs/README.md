# shikosai34 設計書ドキュメント

このディレクトリは、shikosai34 オーガナイゼーション配下の各リポジトリに関する設計書を一元管理する場所です。

## ディレクトリ構成

```
docs/
├── README.md               # このファイル（全体インデックス）
├── _templates/             # 設計書テンプレート
│   ├── architecture.md     # アーキテクチャ設計書テンプレート
│   └── api.md              # API 設計書テンプレート
├── frontend/               # フロントエンド関連リポジトリの設計書
├── backend/                # バックエンド関連リポジトリの設計書
├── database/               # データベース設計書
├── infrastructure/         # インフラ・DevOps 設計書
└── signage/                # サイネージ・配信システム設計書
```

## 設計書の追加方法

1. 対象領域のディレクトリ（例: `frontend/`）に移動する
2. `_templates/` のテンプレートをコピーして命名する
   - 命名規則: `<リポジトリ名>.md` または `<リポジトリ名>/<種別>.md`
3. テンプレートに沿って内容を記述する
4. PR を作成してレビューを受ける

## 各領域の設計書一覧

| 領域 | ディレクトリ | 説明 |
|:--|:--|:--|
| フロントエンド | [frontend/](./frontend/) | Next.js / Astro / Vite 製アプリの設計書 |
| バックエンド | [backend/](./backend/) | Hono / Bun 製 API サーバーの設計書 |
| データベース | [database/](./database/) | PostgreSQL / Redis のスキーマ・ER 図など |
| インフラ | [infrastructure/](./infrastructure/) | Docker / Cloudflare / GitHub Actions の構成設計書 |
| サイネージ | [signage/](./signage/) | OBS / WebRTC / MediaMTX を用いた配信システム設計書 |
