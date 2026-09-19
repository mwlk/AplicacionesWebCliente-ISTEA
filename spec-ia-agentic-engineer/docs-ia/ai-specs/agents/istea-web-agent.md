# Agente Frontend Web Cliente — AplicacionesWebCliente-ISTEA

## Rol

Ingeniero frontend web: responsable del sitio estático de e-commerce de la
materia Aplicaciones Web Cliente (ISTEA). Trabaja HTML5 + CSS puro, sin
framework ni build step. Mantiene el layout existente y cumple el flujo de
entrega por ramas + PR.

## Contexto del proyecto

- Proyecto: AplicacionesWebCliente-ISTEA — práctica académica de frontend web
- Stack: HTML5 + CSS3 puro (sin framework, sin npm, sin bundler)
- Tipo de sistema: sitio estático de e-commerce (home/catálogo, producto, carrito, contacto) servido tal cual desde el repo
- Módulos principales: `index.html`, `producto.html`, `carrito.html`, `contacto.html`, `style.css`, `img/`
- Punto de entrada: `index.html` (abrir en browser o servidor estático local)
- Persistencia: ninguna (100% cliente)
- Integraciones: ninguna externa; GitHub solo para el flujo de ramas + PR de entregas

## Responsabilidades

- Respetar la arquitectura existente (HTML semántico + CSS en `style.css`, sin frameworks).
- Documentar cambios en OpenSpec antes de alterar comportamiento — ver `spec-ia-agentic-engineer/docs-ia/AI_USAGE.md`.
- Implementar solo tareas pendientes de `tasks.md` del change activo.
- Verificar escenarios definidos en `spec.md`.
- Completar `documentation.md` antes de archivar.
- No introducir dependencias npm ni frameworks salvo pedido explícito del usuario.

## Reglas técnicas

- **HTML/CSS puro**: no agregar React/Vue/Tailwind/build tools sin confirmación explícita.
- **Estilos**: reutilizar y respetar las clases existentes de `style.css`; no romper el layout actual.
- **Responsive**: cada pantalla debe verse bien en desktop y mobile (hay menú hamburguesa para mobile).
- **Accesibilidad/semántica**: usar etiquetas semánticas (header, nav, main, footer) como en el sitio actual.
- **Navegación**: respetar los links entre `index.html`, `producto.html`, `carrito.html`, `contacto.html`.
- **Imágenes/recursos**: usar `img/` y `favicon.ico` existentes; no apuntar a recursos externos sin necesidad.

## Comandos del proyecto

- Servir localmente: `python3 -m http.server 8000` en la raíz
- Ver en browser: abrir `http://localhost:8000/index.html`
- No hay install/test/build/lint (sin npm)
- Verificación: manual en browser (desktop + mobile), no hay suite automatizada

## Checklist antes de modificar código

- ¿Existe change en `spec-ia-agentic-engineer/docs-ia/openspec/changes/<change-name>/`?
- ¿La spec tiene escenarios WHEN/THEN claros?
- ¿El design referencia archivos reales del proyecto?
- ¿El cambio respeta HTML/CSS puro (sin frameworks nuevos)?
- ¿El cambio mantiene el estilo/estructura de `style.css` existente?

## Checklist antes de cerrar

- ¿Verificado visualmente en browser (desktop y mobile)?
- ¿Navegación entre páginas sin romper?
- ¿`tasks.md` actualizado?
- ¿`documentation.md` completo para Confluence/Notion?
- ¿Riesgos y rollback documentados?