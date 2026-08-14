# DAGGDeveloper — Sitio personal

Sitio de presentación de **daggdeveloper** (Diego Gómez), enfocado en atraer clientes reales para servicios de desarrollo, sistemas y automatización. Sin frameworks: HTML + CSS + JS puro en un solo archivo.

## Estructura

```
daggdeveloper-portfolio.html   → sitio principal (index)
daggdeveloper-cotizacion.html  → cotizador (archivo aparte, debe subirse junto a este)
favicon.svg                    → ícono de marca
robots.txt                     → indexación para buscadores
sitemap.xml                    → mapa del sitio (dominio placeholder, ver abajo)
README.md                      → este archivo
```

## Desarrollo local

No requiere build. Basta abrir `daggdeveloper-portfolio.html` en el navegador, o servirlo con cualquier servidor estático:

```bash
python3 -m http.server 8000
```

## Deployment

Sube los archivos tal cual a cualquier hosting estático (Netlify, Vercel, GitHub Pages, cPanel). Todos deben ir en el mismo directorio para que los enlaces relativos (cotización, favicon) funcionen.

## Pendientes antes de publicar (checklist)

Estos puntos están marcados en el código con comentarios `<!-- PLACEHOLDER -->` o `[AGREGAR ...]`:

- [ ] **Dominio real**: reemplazar `https://daggdeveloper.cl/` en `<link rel="canonical">`, Open Graph, `robots.txt` y `sitemap.xml` por el dominio definitivo.
- [ ] **Imagen Open Graph** (`assets/img/og-daggdeveloper.jpg`, 1200×630px): crear y subir; referenciada en las etiquetas `og:image` / `twitter:image`.
- [ ] **Foto real** (`assets/img/diego-gomez.webp`): reemplaza el placeholder `👤 //foto.jpg` en el hero. Usa WebP/AVIF, define `width`/`height`, `alt` descriptivo y `loading="lazy"` si no está sobre el pliegue.
- [ ] **Favicon PNG**: `favicon-32x32.png` y `apple-touch-icon.png` (el SVG ya funciona en navegadores modernos, pero conviene tener respaldo PNG para compatibilidad).
- [ ] **Formulario de contacto**: hoy no envía a ningún backend — muestra un mensaje honesto pidiendo escribir por correo. Para conectarlo, usa un servicio como Formspree, Resend o EmailJS (revisar costos antes de decidir), o una función serverless propia.
- [ ] **Google Analytics 4 / Search Console**: no se agregó ningún ID inventado. Cuando tengas cuenta, agrega el snippet de GA4 con tu `G-XXXXXXXXXX` real y verifica el dominio en Search Console.
- [ ] **Redes sociales**: no se linkeó LinkedIn/GitHub/Instagram/YouTube porque no había URLs confirmadas. Agrégalas en la sección de contacto cuando las tengas.
- [ ] **Testimonios**: sección omitida intencionalmente — no hay testimonios reales todavía. Agrégala cuando tengas 1-2 reales; evita completarla con contenido inventado.

## Notas de contenido

- No se inventaron clientes, cifras, testimonios ni resultados medibles. Todo dato mostrado (años de experiencia, stack, ubicación) es el que confirmaste.
- Los niveles de habilidades se muestran como **Avanzado / Intermedio**, no como porcentajes (los porcentajes no tenían respaldo real).
- El proyecto "Landing para Pyme" ya no muestra métricas ficticias (SEO 98/100, conversión +34%, carga 0.8s) — se reemplazó por una descripción honesta de qué busca demostrar la demo.

## Mantenimiento

- El año del footer (`© 2026`) debe actualizarse manualmente cada año.
- Si agregas nuevas secciones, mantén: un solo `<h1>` en toda la página, `<h2>` para cada sección nueva, y contraste/foco visible acorde al resto del sitio.
