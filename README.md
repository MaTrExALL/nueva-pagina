# La Filiberta — rediseño (caso de estudio)

Rediseño de [bufalosargentina.com](https://bufalosargentina.com/) como caso
real para practicar Git y GitHub. Mantiene la identidad de la marca —
humedal, pastizales, más de 20 años de trayectoria— pero consolida en una
sola página bien estructurada el contenido que hoy está repartido (y
repetido) en varias páginas de WordPress.

## Qué se mejoró respecto del sitio original

- El menú de navegación aparecía duplicado en el encabezado; ahora hay uno solo, con versión mobile.
- El contenido de "Inicio" y "Carne de Búfalo" se superponía casi textualmente; ahora cada sección dice algo distinto.
- Se armó una sola página con secciones ancladas (`#carne`, `#productos`, etc.) en vez de 6 páginas separadas con el mismo header repetido.
- El formulario de contacto ahora tiene labels e inputs reales y accesibles (el original no los mostraba).
- Es mobile-first y no depende de WordPress ni de ningún page builder.

## Ver la página en tu computadora

```bash
python3 -m http.server 8000
```

Abrí `http://localhost:8000` en el navegador.

## Estructura del proyecto

```
la-filiberta/
├── index.html
├── css/
│   ├── base.css            # Variables, colores, tipografía global
│   ├── nav.css              # Navegación
│   ├── hero.css             # Sección de bienvenida
│   ├── carne.css            # Sección "La carne de búfalo"
│   ├── productos.css        # Sección "Productos"
│   ├── sustentabilidad.css  # Sección "Sustentabilidad" + "Somos Humedal"
│   ├── galeria.css          # Sección "Galería"
│   ├── contacto.css         # Sección "Contacto"
│   ├── footer.css
│   └── river.css            # Divisor decorativo entre secciones
├── js/
│   └── main.js              # Menú móvil + animación de estadísticas
└── assets/                   # Fotos reales (hoy vacío — ver Pendientes)
```

Cada sección tiene su CSS aparte para que distintos equipos puedan
trabajar en paralelo sin generar conflictos al fusionar ramas.

## Cómo colaboramos

La guía completa de Git y GitHub —rama, commits, pull request, conflictos—
está en [`CONTRIBUTING.md`](./CONTRIBUTING.md).

## Pendientes antes de publicar

- Reemplazar los bloques de color en Hero y Galería por fotos reales del establecimiento.
- Conectar el formulario de contacto a un servicio real de envío de mails.
- Revisar y, si hace falta, actualizar los datos de contacto y redes.
