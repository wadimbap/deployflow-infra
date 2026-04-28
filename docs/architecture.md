# Architecture

## Current State

The current platform runs on a single VPS.

### Running services
- Nginx
- OpenVPN
- Gitea
- Vikunja
- Portainer
- PostgreSQL
- RabbitMQ

## Access

### Public
- 22/tcp
- 80/tcp
- 443/tcp
- 1194/udp

### VPN-only
- Gitea
- Vikunja
- Portainer
- internal admin services

## Planned Migration

### VPS 1
- Nginx
- OpenVPN
- Gitea
- Vikunja
- Portainer

### VPS 2
- PostgreSQL
- RabbitMQ
- SpotFinder backend
- frontend later

## Reasoning

The platform currently uses a single VPS to reduce cost and setup complexity.
The next step is to separate developer tools from runtime and data services.