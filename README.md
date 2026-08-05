# Microservices Proto

This repository contains the shared gRPC contract definitions used by:

- API Gateway
- User Service
- Catalog Service
- Order Service

All services should consume the `.proto` files from this repository. Changes to contracts should be versioned and coordinated across services.