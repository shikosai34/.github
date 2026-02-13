# データベース設計書

PostgreSQL・Redis のスキーマ設計・ER 図・データモデルを管理します。

## 設計書一覧

| 対象 | 説明 | 設計書 |
|:--|:--|:--|
| （追加予定） | | |

## 新規追加方法

```bash
cp docs/_templates/architecture.md docs/database/<リポジトリ名>-schema.md
```

## 記載推奨事項

- ER 図（Mermaid の `erDiagram` を推奨）
- テーブル定義（カラム名・型・制約・説明）
- インデックス設計
- Redis のキー設計（prefix・TTL・用途）
