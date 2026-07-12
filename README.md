# flair-sdk-go

flair-sdk-go is the official Go client SDK for the `flair-core` REST + gRPC API — a thin, dependency-free wrapper that tracks the API contract rather than adding behavior of its own. It's one of FLAIR's integration SDKs; see the [FLAIR org overview](https://github.com/flair-security/.github) for how it fits in.

**Status:** pre-MVP scaffolding, and explicitly on the roadmap ("future") rather than active development yet — sequenced after `flair-core`'s API stabilizes.

## Stack

- Go 1.24+
- Zero external runtime dependencies

## Getting started

```bash
# Build
go build ./...

# Unit tests (no external deps)
go test ./...

# Integration tests (requires a running flair-core instance)
FLAIR_CORE_URL=http://localhost:8080 go test -tags integration ./...

# Linter
golangci-lint run ./...

# Generate from OpenAPI
oapi-codegen -config oapi-codegen.yaml openapi/flair-core-v1.yaml

# Examples
go run examples/list-alerts/main.go
```

## Documentation

Docs live in [flair-docs](https://github.com/flair-security/flair-docs) — the docs site itself is still under construction.

## Contributing

See the org-wide [CONTRIBUTING.md](https://github.com/flair-security/.github/blob/main/CONTRIBUTING.md).

## Security

See the org-wide [SECURITY.md](https://github.com/flair-security/.github/blob/main/SECURITY.md) for how to report vulnerabilities.

## License

Apache License 2.0 — see [LICENSE](LICENSE).
