# WuMama API Contract

Version: v0.6

## Principle

Frontend communicates through defined interfaces.

## Main APIs

Products

GET /products

GET /products/{id}


Orders

POST /orders

GET /orders/{id}


Users

GET /profile

PUT /profile


Admin

GET /admin/orders

PATCH /admin/orders/{id}


## Rules

Every API requires:
- Request format
- Response format
- Authentication rule
- Error handling
