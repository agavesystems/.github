# Cómo trabajamos

Esto aplica a todos los repos de `agavesystems`, salvo que el repo diga otra cosa en su propio `CONTRIBUTING.md`.

## Todo empieza en un issue

- Si no está en un issue, no existe. Ni en un chat, ni en una nota, ni en una tarjeta suelta del tablero.
- El issue va en el repo que lo va a resolver. Un pendiente de la operación que no es de ningún repo va en `agavesystems/jarabe-de-agave`.
- Usa el formulario que corresponda. Lo que llega de un cliente por WhatsApp o correo entra como "Solicitud de cliente".
- Cada issue lleva una prioridad (`p1`, `p2`, `p3`) y un tipo (`tipo:*`). Se ponen al clasificarlo.
- Todo issue entra al tablero de la operación (Project "Jarabe de Agave") en Bandeja. De ahí sale con proyecto y responsable.

## Ramas y commits

- Una rama por issue: `<tipo>/<numero>-<slug>`, por ejemplo `fix/42-webhook-mudo`.
- Commits en Conventional Commits, una línea: `tipo(alcance): resumen`. Sin cuerpo salvo que el cambio lo pida.
- Sin trailers de atribución.

## Pull requests

- Todo cambio entra por PR. En repos de cliente con despliegue continuo, nunca push a `main`.
- El PR sigue la plantilla: qué y por qué, `Cierra #n`, cómo se probó y la revisión de seguridad.
- El CI de la casa tiene que pasar. Las acciones de GitHub se fijan a un SHA completo.
- Quien abre el PR no lo fusiona sin una revisión, salvo en un repo donde trabaja solo.

## Entregas al cliente

Cada proyecto de cliente tiene su Project con hitos, entregas, versiones y roadmap. El estándar está en el README del Project "Plantilla: proyecto de cliente". En corto:

1. Cada entrega es un issue "Entrega: qué (hito)".
2. Sale con un tag y un release.
3. Se cierra cuando el cliente acepta y la evidencia está en `docs/entregables/<hito>/aceptacion.*`.

## Secretos

Nunca en un archivo versionado, ni en un issue, ni en un PR. Si necesitas una variable nueva, va al `.env.example` del repo con valor vacío.
