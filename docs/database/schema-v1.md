# WuMama Database Schema v1.0

版本：v1.0

目的：
建立支援電商、會員、訂單、庫存、CRM、ERP 擴充的資料模型。

Database:
PostgreSQL / Supabase

## Tables

### users
會員資料。

Fields:
- id uuid PK
- email text
- name text
- phone text
- created_at timestamp


### products
商品主檔。

Fields:
- id uuid PK
- sku text
- name text
- description text
- price integer
- cost integer
- status text
- created_at timestamp


### product_variants
商品規格。

Fields:
- id uuid PK
- product_id uuid FK
- name text
- price integer
- stock integer


### orders
訂單主表。

Fields:
- id uuid PK
- user_id uuid FK
- email text
- total_amount integer
- payment_status text
- order_status text
- created_at timestamp


### order_items

取代舊 orders.items JSON。

Fields:
- id uuid PK
- order_id uuid FK
- product_id uuid FK
- variant_id uuid FK
- quantity integer
- price integer


### shipping_addresses

Fields:
- id uuid PK
- order_id uuid FK
- name text
- phone text
- address text


### payments

Fields:
- id uuid PK
- order_id uuid FK
- method text
- status text
- transaction_id text
- created_at timestamp


### inventory

Fields:
- id uuid PK
- product_id uuid FK
- quantity integer
- updated_at timestamp


## Migration Strategy

Phase 1:
新增 products / order_items。

Phase 2:
將舊 orders.items JSON 轉換。

Phase 3:
停止寫入 items。

Phase 4:
移除舊欄位。


## Rule

禁止未確認修改 Schema。
所有變更需同步更新 docs/database。
