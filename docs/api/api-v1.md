# WuMama API Specification v1.0

版本：v1.0

## Product API

GET /products

取得商品列表。


POST /products

建立商品。


GET /products/{id}

取得商品詳細。


## Order API

POST /orders

建立訂單。


GET /orders/{id}

查詢訂單。


GET /users/{id}/orders

查詢會員訂單。


## User API

GET /profile

取得會員資料。


PUT /profile

更新會員資料。


## Admin API

GET /admin/orders

管理訂單列表。


PATCH /admin/orders/{id}

更新訂單狀態。


## Rules

所有 API 必須紀錄：
- Request
- Response
- Authentication
- Error handling
