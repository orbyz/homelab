# ADR-002

## Título

Red Docker compartida.

## Estado

Aceptado.

## Problema

Cada stack creaba su propia red.

Los servicios no podían comunicarse por nombre.

## Decisión

Crear una red Docker externa llamada:

homelab

Todos los stacks utilizan esa red.

## Consecuencias

- DNS interno entre contenedores.
- Comunicación sencilla.
- Arquitectura consistente.
