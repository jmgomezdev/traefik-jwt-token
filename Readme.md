# Traefik JWT Token

Traefik JWT Verify Time

## Configuration

Start with command

```yaml
command:
  - --experimental.plugins.traefik-token-middleware.modulename=github.com/jmgomezdev/traefik-jwt-verify-time
  - --experimental.plugins.traefik-token-middleware.version=v1.0.1
```

Activate plugin in your config

```yaml
spec:
  plugin:
    traefik-jwt-verify-time:
      secret: SECRET
```

JWT fields required:

- jti: JWT id
- iat: Issue at
- exp: Expiration time
