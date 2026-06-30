# HomeLab Architecture

## Objetivo

Construir una infraestructura personal autoalojada basada en Docker que permita disponer de servicios privados, seguros y fáciles de mantener, utilizando Fedora como sistema anfitrión y Portainer como plataforma de administración.

---

# Hardware

**Host**

* HP Engage Flex Pro
* Intel Core i5-8500 (6 núcleos)
* 24 GB RAM
* Fedora Linux 44
* Docker CE
* Portainer CE

---

# Objetivos

* VPN privada para acceso remoto.
* Nube privada para documentos y archivos.
* Sincronización entre ordenadores y móviles.
* Biblioteca privada de fotografías.
* Servidor multimedia.
* Bloqueo de publicidad en toda la red.
* Monitorización de servicios.
* Infraestructura completamente basada en Docker.

---

# Principios

* Todo servicio se ejecutará mediante Docker Compose.
* Cada servicio tendrá su propio directorio dentro de `compose/`.
* Los datos persistentes vivirán en `data/`.
* La infraestructura estará versionada en Git.
* No se instalarán servicios directamente sobre Fedora salvo Docker y sus dependencias.

---

# Estructura del proyecto

```text
homelab/
├── backups/
├── compose/
├── data/
├── docs/
├── scripts/
├── .env
├── .gitignore
└── README.md
```

---

# Roadmap

## Fase 0

* Docker
* Portainer

## Fase 1

* Homepage

## Fase 2

* Uptime Kuma

## Fase 3

* AdGuard Home

## Fase 4

* WireGuard

## Fase 5

* Nginx Proxy Manager

## Fase 6

* Nextcloud

## Fase 7

* Immich

## Fase 8

* Jellyfin

## Fase 9

* Backups automáticos

---

# Reglas del proyecto

1. No improvisar instalaciones.
2. No modificar la arquitectura sin una decisión consciente.
3. Cada fase debe quedar completamente funcional antes de comenzar la siguiente.
4. Todo cambio importante deberá registrarse mediante un commit.
5. La documentación forma parte del proyecto.

---

# Estado actual

* [x] Docker
* [x] Portainer
* [ ] Homepage
* [ ] Uptime Kuma
* [ ] AdGuard Home
* [ ] WireGuard
* [ ] Nginx Proxy Manager
* [ ] Nextcloud
* [ ] Immich
* [ ] Jellyfin
