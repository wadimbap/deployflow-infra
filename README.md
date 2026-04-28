# Deployflow Infra

Self-hosted internal developer platform deployed on VPS.

## Overview

This repository contains sanitized infrastructure configuration and documentation for a self-hosted internal developer platform used as a foundation for SpotFinder.

## Current State

At the moment the platform is running on a single VPS and includes:

- Nginx
- OpenVPN
- Gitea
- Vikunja
- Portainer
- PostgreSQL
- RabbitMQ

## Access Model

### Public
- 80 / 443 — reverse proxy
- 22 — SSH
- 1194/udp — OpenVPN

### VPN-only
- Gitea
- Vikunja
- Portainer
- internal infrastructure services

## Planned Migration

The next infrastructure step is to move application runtime and data services to a second VPS.

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

## Goals

- build a self-hosted internal engineering environment
- restrict internal tools behind VPN
- prepare a clean foundation for SpotFinder backend
- support future CI/CD and staged deployment
- support future migration to a two-VPS layout

## Notes

This repository contains sanitized examples only.
No real secrets, VPN configs, private keys or production credentials are stored here.

## Next Steps

- SpotFinder backend
- CI/CD pipeline
- deployment to second VPS
- frontend integration