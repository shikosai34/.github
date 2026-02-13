# インフラ・DevOps 設計書

Docker・Cloudflare・GitHub Actions を用いたインフラ構成の設計書を管理します。

## 設計書一覧

| 対象 | 説明 | 設計書 |
|:--|:--|:--|
| （追加予定） | | |

## 新規追加方法

```bash
cp docs/_templates/architecture.md docs/infrastructure/<対象名>.md
```

## 記載推奨事項

- インフラ全体構成図
- Docker Compose サービス構成
- Cloudflare Tunnel・Pages・R2 の設定概要
- GitHub Actions ワークフローの概要
- 環境（本番・ステージング）の違い
- シークレット・環境変数の管理方針
