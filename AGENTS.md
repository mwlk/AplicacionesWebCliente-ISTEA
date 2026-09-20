# AGENTS

## Proyecto

Sitio estatico de e-commerce (practica academica ISTEA): HTML + CSS puro, sin JS, sin
npm, sin build/test/lint. El `package.json`/`node_modules` existen solo bajo `.opencode/`
(config del plugin de opencode), no son del proyecto. No hay suite de tests: verificar en
browser con `python3 -m http.server 8000`. Entregas: rama propia + PR a `main` (no directo
sobre `main`, ver `README.MD`).

**Git: sin acciones automaticas.** El agente no hace `commit`, `push` ni crea PRs por su
cuenta: solo cuando el usuario lo pide explicitamente en el mensaje.

## Flujo spec-driven

Este repositorio usa una carpeta unica de trabajo IA: `spec-ia-agentic-engineer/`.

Antes de modificar codigo, leer:

1. `README.MD` del proyecto (nota: extension en mayusculas).
2. `spec-ia-agentic-engineer/README.md`.
3. `spec-ia-agentic-engineer/AGENTS.md`.
4. `spec-ia-agentic-engineer/docs-ia/README.md`.
5. `spec-ia-agentic-engineer/docs-ia/AI_USAGE.md`.
6. `spec-ia-agentic-engineer/docs-ia/PROJECT_CONTEXT.md`.
7. `spec-ia-agentic-engineer/docs-ia/openspec/config.yaml`.
8. El change activo (si existe) en `spec-ia-agentic-engineer/docs-ia/openspec/changes/<change-name>/`.

Reglas:

- Dos modos de change: **full** (`proposal.md`+`design.md`+`tasks.md`+`documentation.md`+`specs/<funcionalidad>/spec.md`, via `/sdd-new`) y **lite** (`lite.md`+`tasks.md`, via `/sdd-new-lite`). Ver criterio de cual usar en `sdd-new.md`/`sdd-new-lite.md`.
- No implementar codigo si falta `tasks.md` y, segun el modo del change activo, falta `lite.md` (modo lite) o `proposal.md`+`design.md`+`specs/<funcionalidad>/spec.md` (modo full).
- Si la feature es ambigua, actualizar la spec antes de programar.
- Mantener cambios chicos y trazables.
- Marcar tareas como completas solo despues de verificar.
- Antes de archivar, completar `documentation.md` para Confluence/Notion.
- Para archivar, usar `spec-archive` o `sdd-archive`: actualizar spec estable si corresponde y mover el change completo de `openspec/changes/` a `openspec/archive/`.
- Mantener todos los artefactos IA dentro de `spec-ia-agentic-engineer/`.

En opencode los comandos slash equivalentes estan en `.opencode/command/`: `/sdd-setup`, `/sdd-new`, `/sdd-new-lite`, `/sdd-apply`, `/sdd-review`, `/sdd-document`, `/sdd-archive`.