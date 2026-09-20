# Tasks: sidebar-navegacion-ocultable

## 0. Revision de contexto

- [x] 0.1 Leer `README.MD` del proyecto, `spec-ia-agentic-engineer/AGENTS.md`, `spec-ia-agentic-engineer/docs-ia/PROJECT_CONTEXT.md` y `spec-ia-agentic-engineer/docs-ia/openspec/config.yaml`.
- [x] 0.2 Inspeccionar patrones existentes (`style.css`, las 5 paginas `.html`).
- [x] 0.3 Identificar archivos afectados: `style.css` (principal) y ajustes minimos en `index.html`, `producto.html`, `carrito.html`, `contacto.html`, `nosotros.html`.

## 1. Implementacion

### 1.1 Variables CSS en `:root`

- [ ] 1.1.1 Definir al menos 6 variables en `:root` comentadas/explicadas: colores (fondo, texto, marca, marca-oscuro, acento, borde, seleccion), tipografia (familia y tamanos), espaciado (gap/padding: chico, medio, grande) y radio de borde.
- [ ] 1.1.2 Reemplazar valores magicos de `style.css` por las variables en header, nav, main y footer (estilo propio de cada componente).
- [ ] 1.1.3 Mantener la paleta/estructura actual (los valores se conservan como variables; no cambia el look actual).

### 1.2 Navbar desktop (logo izquierda, links centrados, boton derecha)

- [ ] 1.2.1 Acomodar header/nav en desktop como barra horizontal: logo a la izquierda, links centrados y boton a la derecha (`display: flex` + `gap`).
- [ ] 1.2.2 Boton a la derecha: label hamburguesa y/o CTA segun corresponda en desktop; mantener estilo de boton existente.

### 1.3 Sidebar / drawer mobile ocultable

- [ ] 1.3.1 Convertir el menu de navegacion del mobile en panel lateral (drawer) oculto por defecto que se abre con `#menu-toggle:checked` (checkbox hack) y hamburguesa a "X".
- [ ] 1.3.2 Asegurar que el drawer no desplace el contenido (overlay o desplazamiento con transicion) y que cierre al volver a tocar la hamburguesa.
- [ ] 1.3.3 Eliminar la franja navbar vacia que quedaba en mobile con el menu colapsado.

### 1.4 Catalogo en grid responsive (1/2/3)

- [ ] 1.4.1 Pasar `#catalogo .productos` de flex a `display: grid`.
- [ ] 1.4.2 Grid responsive con media queries: 1 columna (base/mobile), 2 columnas (>=600px tablet) y 3 columnas (>=1024px desktop).
- [ ] 1.4.3 Ajustar gap y tamaños de tarjetas para que el grid 1/2/3 se vea bien.

### 1.5 Responsive mobile/tablet (UX/UI)

- [ ] 1.5.1 Revisar espaciados/padding de header, nav, main y footer en mobile y tablet usando las variables nuevas.
- [ ] 1.5.2 Verificar tablet (>=600px): catalogo 2 columnas y nav/header comodamente legibles.
- [ ] 1.5.3 Mantener buscador, sidebar de filtros (`index.html`), tablas y formularios funcionales.

## 2. Validacion

- [ ] 2.1 No aplica tests automatizados (proyecto estatico sin suite). Verificacion estatica + HTTP 200 de las 5 paginas y assets con `python3 -m http.server 8000`.
- [ ] 2.2 Verificacion visual manual en browser (mobile, tablet, desktop) de las 5 paginas: barra desktop (logo/links/boton), drawer mobile con hamburguesa, catalogo 1/2/3.
- [ ] 2.3 Confirmar los escenarios de `lite.md` cubiertos (variables `:root`, nav flex, drawer mobile, grid 1/2/3, consistencia entre paginas).

## 3. Cierre

- [ ] 3.1 Decidir si se corre `/sdd-document` (genera `documentation.md` para Confluence/Notion) o alcanza con `tasks.md` + `lite.md`.
- [ ] 3.2 Evaluar si el change crecio y amerita full (`proposal.md`/`design.md`/`specs/<funcionalidad>/spec.md`); de crecer la implementacion, escalar.
- [ ] 3.3 Archivar con `/sdd-archive` cuando este listo.