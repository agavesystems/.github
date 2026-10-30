# Cómo trabajamos

Esto aplica a todos los repos de `agavesystems`, salvo que el repo diga otra cosa en su propio `CONTRIBUTING.md`.

## Todo empieza en un issue

- Si no está en un issue, no existe. Ni en un chat, ni en una nota, ni en una tarjeta suelta del tablero.
- Un issue abierto dice que falta algo, y nada más. Un hallazgo va al `docs/` del repo, una idea sin dueño a Discussions, y lo que ya pasó al PR o a un ADR.
- Antes de abrir uno, busca si ya existe. Un plan se abre como una épica; cada rebanada se abre como sub-issue cuando se empieza.
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
- El PR sigue la plantilla: qué y por qué, `Closes #n`, cómo se probó y la revisión de seguridad. La palabra clave va en inglés porque GitHub no reconoce "Cierra". Si el PR solo avanza el issue, `Avanza #n`. `gh pr create --body` se salta la plantilla, así que la línea se escribe a mano.
- El issue se cierra al fusionar o desplegar, nunca "cuando el cliente lo valide".
- El CI de la casa tiene que pasar. Las acciones de GitHub se fijan a un SHA completo.
- Quien abre el PR no lo fusiona sin una revisión, salvo en un repo donde trabaja solo.

## Entregas al cliente

Una entrega no es un issue: ya pasó, y la cola es para lo que falta (ADR 016 de `agave-core`).

1. Cada hito con el cliente es un Milestone del repo.
2. Cada entrega sale con un tag y un Release. Las notas del release dicen qué salió.
3. `docs/compromiso.md` lleva la tabla de entregas: qué, cuándo, el release y el estado de aceptación. La evidencia de la aceptación va en `docs/entregables/<hito>/aceptacion.*`.

## Secretos

Nunca en un archivo versionado, ni en un issue, ni en un PR. Si necesitas una variable nueva, va al `.env.example` del repo con valor vacío.
