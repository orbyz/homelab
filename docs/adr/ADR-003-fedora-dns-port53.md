# ADR-003

## Título

Liberación del puerto 53 en Fedora 44.

## Estado

Aceptado.

## Problema

Docker no podía publicar el puerto 53 para AdGuard Home.

## Contexto

Fedora 44 utiliza systemd-resolved con DNS Stub habilitado.

El puerto 53 quedaba reservado para el resolvedor local.

## Alternativas consideradas

1. Desactivar systemd-resolved.
2. Utilizar macvlan.
3. Configurar correctamente systemd-resolved.

## Decisión

Mantener systemd-resolved.

Crear:

/etc/systemd/resolved.conf.d/adguard.conf

Contenido:

DNSStubListener=no

Posteriormente reiniciar:

- systemd-resolved
- Docker

## Consecuencias

- Docker puede utilizar el puerto 53.
- Fedora mantiene su resolución DNS.
- Solución compatible con futuras actualizaciones.
