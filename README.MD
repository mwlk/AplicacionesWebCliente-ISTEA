# La Casa de los Hilos

E-commerce estático de artículos textiles (hilos, lanas, telas, kits de tejido),
desarrollado como práctica académica de la materia Aplicaciones Web Cliente (ISTEA).

## Arquitectura

Sitio web de cliente: **HTML + CSS + JS** puros, servido tal cual desde el repo
(GitHub Pages / servidor estático). **Supabase** como backend-as-a-service
planificado (tablas, auth, storage) que se integrará en iteraciones posteriores.

- **Sin build step, sin bundler, sin dependencias npm**: el HTML/CSS/JS se sirve
  tal cual. El cliente de Supabase (si se usa) se cargará vía CDN (import ESM).
- **Sin framework del lado del cliente**: JS vanilla en `js/`.
- **Estructura de datos**: se define en un change/tabla de Supabase aparte; por
  ahora el catálogo es estático en el HTML.

## Estructura de archivos

```
AplicacionesWebCliente-ISTEA/
├── index.html        # landing + catálogo de artículos textiles (header, filtros, catálogo, footer)
├── producto.html     # detalle de un artículo textil con especificaciones
├── carrito.html      # carrito de compras + formulario para finalizar la compra
├── contacto.html     # formulario de contacto + información de la tienda
├── nosotros.html     # sección "quiénes somos"
├── style.css         # estilos de todo el sitio (header, nav, footer, catálogo, responsive)
├── js/
│   └── main.js       # script base (placeholder; sin lógica de negocio todavía)
├── img/              # imágenes (ej. placeholder.svg; logo real pendiente)
├── favicon.ico
├── Predictions.md    # lista de prácticas del curso (backlog)
├── README.MD
└── spec-ia-agentic-engineer/   # flujo spec-driven (docs IA, ver AGENTS.md)
```

## Layout común

Todas las páginas comparten:

- **Header** con branding "La Casa de los Hilos".
- **Navbar** (Inicio, Catálogo, Nosotros, Carrito, Contacto), colapsable en
  mobile con menú hamburguesa (solo HTML/CSS).
- **Footer** con copyright y redes sociales.
- **Responsive**: desktop (catálogo en 4 columnas con sidebar de filtros),
  tablet (3 columnas) y mobile (1 columna, nav colapsada).

## Cómo correrlo

```bash
python3 -m http.server 8000
```

Abrir `http://localhost:8000/index.html` en el browser (desktop y mobile).
No hay install/test/build/lint: la validación es manual en browser.

## Flujo de entregas

Cada práctica se trabaja en una rama y se integra por **PR contra `main`**
(ver el resto de este README).