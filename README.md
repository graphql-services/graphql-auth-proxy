# graphql-auth-proxy

Authorization proxy for GraphQL server. JWT is expected as access token and JWKs endpoint is required for downloading public keys for validation.

- `PROXY_URL` – URL of server for proxying valid requests
- `JWKS_PROVIDER_URL` – JWKs endpoint (eg. `https://example.com/.well-known/jwks.json`)
- `REQUIRED_JWT_SCOPES` – space-separated list of scopes required to be present in JWT access token

# Token scopes

JWT token with custom `scope` claim is expected. This claim should contain all approved scopes.
Currently the introspection endpoint is not supported.
