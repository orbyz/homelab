# Journal

---

## 2026-07-01

### Objetivo

Instalar AdGuard Home.

### Problema encontrado

Docker no podía publicar el puerto 53.

### Investigación

Se comprobó que:

- Docker Compose era correcto.
- Portainer era correcto.
- El conflicto provenía del host.

Fedora 44 utilizaba `systemd-resolved` con DNS Stub.

### Solución

Se creó un drop-in:

/etc/systemd/resolved.conf.d/adguard.conf

Contenido:

DNSStubListener=no

Posteriormente se reinició:

systemctl restart systemd-resolved

Después:

systemctl restart docker

Docker pudo publicar correctamente el puerto 53.

### Aprendido

- Cómo funciona systemd-resolved.
- Diferencia entre DNS del host y DNS interno de Docker.
- Por qué no modificar archivos en /usr/lib/systemd.
