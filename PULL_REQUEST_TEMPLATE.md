<!--
Título en Conventional Commits, una línea: tipo(alcance): resumen
Tipos: feat, fix, docs, chore, refactor, revert. Ejemplo: fix(webhook): el router contesta 200 al test sintético
Sin trailers de atribución ni "generado por".
-->

## Qué y por qué

<!-- Qué cambia y qué problema resuelve. Dos o tres frases. -->

<!-- La palabra clave va en inglés: GitHub no cierra el issue con "Cierra". Si el PR solo avanza el issue, escribe "Avanza #n". -->
Closes #

## Tipo

- [ ] Falla corregida
- [ ] Capacidad nueva
- [ ] Trabajo sin cambio de comportamiento
- [ ] Documentación o expediente
- [ ] Rompe algo que ya existía (explica abajo qué y cómo se migra)

## Cómo se probó

<!-- Los comandos que corriste y lo que salió. "Debería funcionar" no cuenta. -->

```bash

```

## Seguridad

- [ ] Sin secretos, tokens ni `.env` en el diff
- [ ] Sin rutas de una máquina (`/Users/...`) ni puertos fijos
- [ ] Sin datos personales del cliente en código, pruebas o fixtures

## Entrega

<!-- Solo si este PR es parte de una entrega al cliente. -->

- Issue de entrega: #
- Versión que sale con esto:

## Para quien revisa

<!-- Dónde mirar con más cuidado, y lo que queda para otro PR. -->
