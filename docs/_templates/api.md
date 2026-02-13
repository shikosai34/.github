# [リポジトリ名] API 設計書

> **最終更新:** YYYY-MM-DD
> **担当者:** @GitHub-username
> **ベース URL:** `https://api.example.com`

---

## 1. 概要

<!-- この API が提供する機能の概要を説明してください -->

## 2. 認証方式

<!-- 認証方法（Bearer Token, Session, など）を記載してください -->

## 3. 共通仕様

### リクエストヘッダー

| ヘッダー | 値 | 必須 |
|:--|:--|:--:|
| `Content-Type` | `application/json` | ✓ |
| `Authorization` | `Bearer <token>` | 認証が必要なエンドポイントのみ |

### レスポンス形式

```json
{
  "data": {},
  "error": null
}
```

### エラーレスポンス

```json
{
  "data": null,
  "error": {
    "code": "ERROR_CODE",
    "message": "エラーの説明"
  }
}
```

---

## 4. エンドポイント一覧

### [リソース名]

#### `GET /resource`

**説明:** リソースの一覧を取得します。

**クエリパラメータ:**

| パラメータ | 型 | 必須 | 説明 |
|:--|:--|:--:|:--|
| `limit` | `number` | | 取得件数（デフォルト: 20） |
| `offset` | `number` | | オフセット（デフォルト: 0） |

**レスポンス例:**

```json
{
  "data": []
}
```

---

#### `POST /resource`

**説明:** リソースを作成します。

**リクエストボディ:**

```json
{
  "field": "value"
}
```

**レスポンス例:**

```json
{
  "data": {
    "id": "xxx",
    "field": "value"
  }
}
```

---

## 5. エラーコード一覧

| コード | HTTP ステータス | 説明 |
|:--|:--:|:--|
| `UNAUTHORIZED` | 401 | 認証が必要です |
| `FORBIDDEN` | 403 | アクセス権限がありません |
| `NOT_FOUND` | 404 | リソースが見つかりません |
| `VALIDATION_ERROR` | 422 | 入力値が不正です |
| `INTERNAL_ERROR` | 500 | サーバー内部エラーです |
