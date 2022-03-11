# Traefik JWT Token

Traefik JWT Token.

## Configuration

Start with command

```yaml
command:
  - --experimental.plugins.traefik-token-middleware.modulename=github.com/jmgomezdev/traefik-jwt-token
  - --experimental.plugins.traefik-token-middleware.version=v1.0.0
```

Activate plugin in your config

```yaml
spec:
  plugin:
    traefik-jwt-token:
      secret: SECRET
```

JWT fields required:

- jti: JWT id
- iat: Issue at
- exp: Expiration time
