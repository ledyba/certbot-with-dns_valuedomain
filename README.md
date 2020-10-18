# Certbot with Value Domain DNS Plugin (Experimental)

[![Publish Docker image](https://github.com/ledyba/certbot-with-dns_valuedomain/workflows/Publish%20Docker%20image/badge.svg)](https://github.com/ledyba/certbot-with-dns_valuedomain/actions?query=workflow%3A%22Publish+Docker+image%22)

## How to use

Docker image is avaiable at `ghcr.io/ledyba/certbot-with-dns_valuedomain:latest`

### docker-compose.yml example

```yaml
---
version: '3.7'

services:
  certbot:
    image: 'ghcr.io/ledyba/certbot-with-dns_valuedomain:latest'
    net: 'host'
    volumes:
      - ./data:/etc/letsencrypt
      - ./conf:/etc/certbot

networks: {}
```

then, run

```bash
docker-compose run --rm certbot help
```