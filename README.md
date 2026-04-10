# AP2 Proto Repository

This repository contains **only** `.proto` files for the AP2 Assignment 2 project.

## Structure

```
├── payment/
│   └── payment.proto    # PaymentService: ProcessPayment RPC
└── order/
    └── order.proto      # OrderService: SubscribeToOrderUpdates (Server-side Streaming)
```

## How it works (Contract-First Flow)

1. Developer edits `.proto` files here and pushes to `main`.
2. GitHub Actions in the **Generated Code Repository** detects changes.
3. `protoc` generates `.pb.go` and `_grpc.pb.go` files automatically.
4. Generated code is pushed to the Generated repo with a tagged release.
5. Services import via `go get github.com/YOUR_GITHUB_USER/ap2-proto-generated@v1.0.0`.

## Related Repositories

- **Generated Code**: `github.com/YOUR_GITHUB_USER/ap2-proto-generated`
- **Main Project**: `github.com/YOUR_GITHUB_USER/ap2-assignment`
