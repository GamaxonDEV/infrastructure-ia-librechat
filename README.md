# InfrastructureIA

Plateforme IA personnelle basée sur **LibreChat**, déployée avec Docker Compose sous Windows.

## Fonctionnalités

- Modèles locaux via **Ollama** (hôte Windows)
- Modèles cloud gratuits via **OpenRouter**
- Recherche web : **SearXNG**, **Firecrawl** (scraping) et **Jina** (reranking)
- Historique indexé avec **Meilisearch**
- Accès distant HTTPS via **Traefik** et Let's Encrypt (challenge DNS OVH), ainsi que **Tailscale**
- Branding personnalisé (image `Dockerfile.librechat`)

## Services

| Conteneur | Rôle |
|---|---|
| infra-mongodb | Base de données |
| infra-meilisearch | Recherche dans l'historique |
| librechat | Interface de chat (port 3080) |
| searxng | Moteur de recherche local |
| traefik | Reverse proxy HTTPS |

## Installation

1. Cloner le dépôt :
   ```powershell
   git clone <url-du-depot> C:\InfrastructureIA
   cd C:\InfrastructureIA
