# Decisiones de Arquitectura

## D001
La infraestructura se define mediante Docker Compose y se despliega desde Git usando Portainer.

## D002
Los datos persistentes se almacenan en:
/home/OrByZ/workspace/infrastructure/homelab/data

## D003
Cada servicio tendrá:

- compose/<servicio>/
- data/<servicio>/

## D004
Todo cambio seguirá el flujo:

Editar
↓
Validar
↓
Commit
↓
Push
↓
Deploy desde Portainer
↓
Verificar
