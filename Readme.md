#  Traefik JWT Token

 Traefik JWT Token  

## Configuration

Start with command
```yaml
command:
  - --experimental.plugins.traefik-token-middleware.modulename=github.com/tonyfud/traefik-jwt-token
  - --experimental.plugins.traefik-token-middleware.version=v0.2.2
```

Activate plugin in your config  

```yaml
apiVersion: traefik.containo.us/v1alpha1
kind: Middleware
metadata:
  name: jwt-token
spec:
  plugin:
    traefik-jwt-token:
      secret: 112233
```
