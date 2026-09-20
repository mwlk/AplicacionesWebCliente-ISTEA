# Contexto del proyecto: AplicacionesWebCliente-ISTEA

> Archivo completado por /sdd-setup y actualizado por el change `la-casa-de-los-hilos` (2026-09-19).

## Qué es

E-commerce estático de artículos textiles: **"La Casa de los Hilos"** (hilos,
lanas, telas, kits de tejido y accesorios). Práctica académica de la materia
Aplicaciones Web Cliente (ISTEA). Site de cliente con layout típico de tienda
online: landing/catálogo, detalle de producto, carrito y contacto.

## Stack detectado

- **HTML5** puro: `index.html` (landing + catálogo con filtros), `product.html`
  (detalle + especificaciones), `cart.html`, `contact.html`, `about.html`
- **CSS** puro: `style.css` (header, navbar, catálogo, footer, responsive)
- **JS** vanilla: `js/main.js` (base/placeholder, sin lógica de negocio todavía)
- **Supabase** (planificado, no conectado aún): backend-as-a-service para
  catálogo/origen de datos en iteraciones futuras
- Sin framework, sin build step, sin bundler, sin dependencias npm — se sirve tal
  cual desde el repo (GitHub Pages / estático)
- `img/` y `favicon.ico`: recursos estáticos
- `Predictions.md`: lista de prácticas pendientes/realizadas del curso

## Estructura

```
AplicacionesWebCliente-ISTEA/
├── index.html        # landing: header + filtro categorias + catalogo + footer
├── product.html     # detalle de articulo textil con especificaciones
├── cart.html      # pantalla de carrito + formulario de compra
├── contact.html     # pantalla de contacto
├── about.html     # seccion "quiénes somos"
├── style.css         # estilos de todo el sitio
├── js/main.js        # script base (placeholder)
├── img/              # imágenes (ej. placeholder.svg; logo real pendiente)
├── favicon.ico
├── Predictions.md    # lista de prácticas del curso
└── .github/          # pull_request_template
```

## Puntos de entrada

- `index.html` — abrir en browser directamente (o servir la carpeta por HTTP local)
- No hay scripts de build ni servidor de desarrollo: se ve con `python -m http.server` o abriendo el archivo

## Persistencia

- Cliente: ninguna (catálogo estático en el HTML).
- Planificado: Supabase (tablas de productos/contacto/carrito, auth, storage) en
  un change futuro. No conectado todavía.

## Integraciones externas

- Supabase: planificado (sin integración actual). GitHub Actions: solo forma del
  repo template (flujo PR para entregas).

## Convenciones de errores

- Sin capa de errores de backend. Validación de formularios del lado cliente (HTML nativo) si corresponde.
- Mantener HTML semántico y accesible (materia de frontend web).
- **Accesibilidad (WCAG AAA)**: todo texto debe cumplir contraste ≥ 7:1 sobre su
  fondo. Los colores viven como tokens en `:root` (`style.css`) y están calibrados
  para AAA; no usar valores de color fuera de los tokens (ni modificar los tokens
  sin recalcular el contraste de cada par afectado).

## Convenciones de tests

- No hay suite de tests automatizados. La validación es manual en browser: navegación entre páginas, filtros, responsive.
- "Hecho" = verificado en browser real (desktop + mobile) y código consistente con `style.css` existente.

## Comandos útiles

- Servir localmente: `python3 -m http.server 8000` (o abrir el `index.html` en el browser)
- No hay lint/build/test de npm.

## Reglas del proyecto

- No introducir framework, build step ni dependencias npm a menos que se pida explícitamente — es HTML/CSS/JS puro.
- Mantener el diseño y clases de `style.css` existentes; no romper el layout actual.
- Cada entrega se trabaja en una rama y se integra por PR contra `main` (flujo de la materia, ver `README.MD`).
- `Predictions.md` lista las prácticas; usarla como backlog de features si corresponde.