# Contexto del proyecto: AplicacionesWebCliente-ISTEA

> Archivo completado por /sdd-setup. Refleja la arquitectura real del proyecto (2026-09-19).

## Qué es

Sitio web estático de e-commerce desarrollado como práctica académica de la
materia Aplicaciones Web Cliente (ISTEA). Es un template de repositorio para
cada alumno: páginas HTML/CSS puras (sin framework), con layout típico de
tienda online: home con catálogo, detalle de producto, carrito y contacto.
No hay backend ni base de datos — todo es cliente.

## Stack detectado

- **HTML5** puro: `index.html` (home con encabezado, filtro de categorías, catálogo y footer), `producto.html` (detalle + especificaciones), `carrito.html`, `contacto.html`
- **CSS** puro: `style.css` (estilos header, catálogo, nav, footer, responsive)
- **Sin framework, sin build step, sin bundler, sin dependencias npm** — se sirve tal cual desde el repo (GitHub Pages / estático)
- `img/` y `favicon.ico`: recursos estáticos
- `Predictions.md`: lista de prácticas pendientes/realizadas del curso

## Estructura

```
AplicacionesWebCliente-ISTEA/
├── index.html        # home: header + filtro categorias + catalogo + footer
├── producto.html     # detalle de producto con especificaciones
├── carrito.html      # pantalla de carrito
├── contacto.html     # pantalla de contacto
├── style.css         # estilos de todo el sitio
├── img/              # imágenes (ej. logo.png)
├── favicon.ico
├── Predictions.md    # lista de prácticas del curso
└── .github/          # pull_request_template
```

## Puntos de entrada

- `index.html` — abrir en browser directamente (o servir la carpeta por HTTP local)
- No hay scripts de build ni servidor de desarrollo: se ve con `python -m http.server` o abriendo el archivo

## Persistencia

- Ninguna. Sitio 100% estático/cliente. Sin backend, sin base de datos, sin localStorage obligatorio.

## Integraciones externas

- Ninguna de terceros. GitHub Actions: solo forma del repo template (flujo PR para entregas).

## Convenciones de errores

- Sin capa de errores de backend. Validación de formularios del lado cliente (HTML nativo) si corresponde.
- Mantener HTML semántico y accesible (materia de frontend web).

## Convenciones de tests

- No hay suite de tests automatizados. La validación es manual en browser: navegación entre páginas, filtros, responsive.
- "Hecho" = verificado en browser real (desktop + mobile) y código consistente con `style.css` existente.

## Comandos útiles

- Servir localmente: `python3 -m http.server 8000` (o abrir el `index.html` en el browser)
- No hay lint/build/test de npm.

## Reglas del proyecto

- No introducir framework, build step ni dependencias npm a menos que se pida explícitamente — es HTML/CSS puro.
- Mantener el diseño y clases de `style.css` existentes; no romper el layout actual.
- Cada entrega se trabaja en una rama y se integra por PR contra `main` (flujo de la materia, ver `README.MD`).
- `Predictions.md` lista las prácticas; usarla como backlog de features si corresponde.