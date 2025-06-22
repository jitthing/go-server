```bash
myapp/
├── cmd/                   
│   └── server/            # entrypoint: main.go (bootstraps app, loads config, starts Gin)
├── internal/              # private application code
│   ├── config/            # env/config loaders
│   ├── router/            # Gin route definitions & middleware wiring
│   ├── server/            # HTTP server setup
│   └── bootstrap/         # dependency injection / app wiring
├── api/                   # request/response DTOs, Swagger/OpenAPI specs
│   ├── v1/                
│   │   ├── handler/       # Gin handlers (controllers)
│   │   └── dto/           # input/output structs
├── domain/                # core business types & interfaces
│   ├── model/             # entity definitions
│   └── service/           # domain service interfaces
├── usecase/               # application logic orchestrating domain & infra
│   └── user/              # e.g. CreateUser, AuthenticateUser
├── repository/            # implementations of domain interfaces
│   ├── mysql/             # MySQL-specific repos
│   └── redis/             # Redis cache clients
├── pkg/                   # shared libraries (logger, errors, middleware)
│   ├── logger/
│   └── middleware/
├── migrations/            # database migration files
├── scripts/               # helper scripts (e.g. codegen, DB seed)
├── deployments/           # k8s manifests, Dockerfiles, CI config
└── docs/                  # design docs, architecture diagrams
```
