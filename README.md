# steveinator-demo

Página estática para probar cosas en el server de Hermes. Se publica con un túnel reverso de TunnelsManager y aparece en https://stevearagonsite.com/tunnels.

```sh
python3 -m http.server 8080 --bind 127.0.0.1   # en el server corre como steveinator-demo.service
curl -X POST http://localhost:4400/tunnels -H "Content-Type: application/json" -H "x-api-key: $TUNNEL_API_KEY" \
  -d '{"name": "steveinator", "localPort": 8080}'
```
