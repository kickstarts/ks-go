# About

This is a simple project to learn how to structure a Go project.

# Project Structure

```bash
project-name/
├── cmd/ # Pontos de entrada da aplicação
│ ├── api/
│ │ └── main.go # Executável principal (e.g., servidor HTTP)
├── internal/ # Código privado específico do projeto
│ ├── domain/ # Entidades e regras de negócio (Core)
│ │ ├── model.go # Definição de structs (e.g., User, Order)
│ │ └── repository.go # Interfaces de repositórios
│ ├── service/ # Serviços que implementam regras de negócio
│ │ ├── user_service.go
│ │ └── email_service.go
│ ├── repository/ # Implementações das interfaces (e.g., banco de dados)
│ │ ├── user_repo.go
│ │ └── order_repo.go
│ ├── handler/ # Handlers (controladores para HTTP/CLI/etc.)
│ │ ├── user_handler.go
│ │ └── order_handler.go
│ ├── middleware/ # Middlewares (e.g., autenticação, logs)
│ └── util/ # Funções utilitárias (helpers, validações, etc.)
├── pkg/ # Pacotes reutilizáveis (públicos ou internos)
│ └── logger/ # Exemplo: wrapper para logging
├── configs/ # Arquivos de configuração (JSON, YAML, etc.)
│ ├── app.yaml
│ └── db.yaml
├── api/ # Arquivos de especificação de API (Swagger/OpenAPI)
│ └── openapi.yaml
├── scripts/ # Scripts úteis (deploy, build, etc.)
│ ├── build.sh
│ └── migrate.sh
├── test/ # Testes integrais e mocks
│ ├── integration/
│ │ └── user_test.go
│ └── mocks/
│ └── user_repo_mock.go
├── go.mod # Arquivo de dependências (Módulos Go)
├── go.sum # Checksum das dependências
└── README.md # Documentação do projeto
```

# Run

```bash
go run cmd/api/main.go
```

# Build

```bash
go build -o bin/api cmd/api/main.go
```

# License

MIT
