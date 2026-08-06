# Microservices Proto

This repository contains the shared gRPC contract definitions used by:

- API Gateway
- User Service
- Catalog Service
- Order Service

## Structure

```text
proto/
├── user.proto
├── catalog.proto
└── order.proto
```

Each service loads the required `.proto` file from this repository.

## Services

### User Service

- CreateUser
- GetUserById
- UpdateUser
- DeleteUser
- ListUsers

### Catalog Service

- CreateCategory
- GetCategoryById
- UpdateCategory
- DeleteCategory
- ListCategories
- CreateProduct
- GetProductById
- UpdateProduct
- DeleteProduct
- ListProducts

### Order Service

- CreateOrder
- GetOrderById
- UpdateOrderStatus
- DeleteOrder
- ListOrders

## Notes

- Each `.proto` file is independent.
- Every service defines its own request and response messages.
- `google.protobuf.Empty` is used for delete and list operations where appropriate.
- Any changes to a `.proto` file should be reflected in all services that use it.