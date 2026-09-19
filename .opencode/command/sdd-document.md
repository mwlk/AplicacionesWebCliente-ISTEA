---
description: Completar documentation.md de un change para Confluence/Notion (solo documentacion).
---

# sdd-document - Cierre Confluence / Notion

Uso:

```text
/sdd-document CHANGE_NAME="<nombre-carpeta-en-changes>"
```

No implementar features salvo pedido explicito. Solo documentacion.

---

Estas trabajando en la raiz del proyecto.

## 0. Argumentos

Parsear los argumentos del usuario desde `$ARGUMENTS`. Los valores disponibles son:

- `CHANGE_NAME`

Si no se pasa `CHANGE_NAME`, listar carpetas en `spec-ia-agentic-engineer/docs-ia/openspec/changes/` y pedir al usuario que elija.

## 1. Detectar modo

Si existe `spec-ia-agentic-engineer/docs-ia/openspec/changes/<CHANGE_NAME>/lite.md` -> modo **lite**.
Si no existe -> modo **full**.

## 2. Leer contexto

1. `spec-ia-agentic-engineer/docs-ia/openspec/_templates/documentation.md`
2. `spec-ia-agentic-engineer/docs-ia/PROJECT_CONTEXT.md`
3. `spec-ia-agentic-engineer/docs-ia/ai-specs/agents/*.md`
4. Modo lite: `spec-ia-agentic-engineer/docs-ia/openspec/changes/<CHANGE_NAME>/lite.md`. Modo full: `.../proposal.md` + `.../design.md`
5. `spec-ia-agentic-engineer/docs-ia/openspec/changes/<CHANGE_NAME>/tasks.md`
6. `spec-ia-agentic-engineer/docs-ia/openspec/changes/<CHANGE_NAME>/specs/**/*.md` si existe
7. `spec-ia-agentic-engineer/docs-ia/openspec/changes/<CHANGE_NAME>/reports/**/*` si existe
8. Codigo o archivos referenciados por design/tasks/lite, solo lectura

## 3. Objetivo

Completar o mejorar:

```text
spec-ia-agentic-engineer/docs-ia/openspec/changes/<CHANGE_NAME>/documentation.md
```

Debe tener las 6 secciones del template:

1. Que problema resuelve
2. Como deberia funcionar
3. Que se modifico
4. Como probarla
5. Que impacto tiene
6. Como mantenerla en el futuro

## 4. Reglas

- Markdown puro, sin HTML.
- No inventar evidencia; si falta prueba, marcar pendiente.
- Incluir scripts, migraciones o configuracion si aplica.
- Usar el agente del proyecto para respetar lenguaje tecnico, arquitectura, riesgos y checklist.
- Si no hay cambios de datos/esquema, decirlo explicitamente.
- No editar codigo productivo.

## 5. Cierre

Indicar si queda:

- LISTA PARA CONFLUENCE / NOTION
- LISTA CON PENDIENTES