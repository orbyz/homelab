# Convenciones del HomeLab

## Docker Compose

Todos los servicios deberán cumplir las siguientes reglas.

### Container

Cada servicio tendrá un nombre fijo.

```yaml
container_name: nombre-del-servicio
```

### Restart

```yaml
restart: unless-stopped
```

### Datos persistentes

Todos los datos vivirán en:

```text
/home/OrByZ/workspace/infrastructure/homelab/data/
```

Ejemplo:

```yaml
volumes:
  - /home/OrByZ/workspace/infrastructure/homelab/data/homepage:/app/config
```

### Redes

Todos los servicios estarán conectados a la red:

```text
homelab
```

Ejemplo:

```yaml
services:
  servicio:
    networks:
      - homelab

networks:
  homelab:
    external: true
```

### Flujo de trabajo

1. Editar
2. Validar (`docker compose config`)
3. Commit
4. Push
5. Pull and Redeploy desde Portainer
6. Verificar
