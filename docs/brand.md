# Marca y estilos — Fundación ChiChiCa

Fuente: `ChiChiCa - Brandbook (1) (1).pdf` (Lineamientos Gráficos 2019, CMYK, sin valores hex ni Pantone). Los hex de abajo son conversiones a pantalla, no valores oficiales.

## Colores

Todos los colores viven como variables CSS en `src/styles/global.css`. No usar hex sueltos en páginas; usar `var(--color-…)`.

| Variable | Valor | Nota |
| :-- | :-- | :-- |
| `--color-accent` / `--color-accent-500` | `#F26A1B` | Naranja de marca (CMYK 1/57/93/0). Botones, banner de impacto, `theme-color` |
| `--color-accent-100…900` | `#fff1e8` → `#3b1a00` | Escala derivada del naranja; 900 es el marrón del contorno del logo |
| `--color-accent-2` | `#7a8a5e` | Verde secundario del sitio |
| `--color-bg` / `--color-surface` | `#f5ead8` / `#ebddc5` | Fondos crema |

Pendiente: el verde del brandbook (`~#117703`, CMYK 91/34/98/29) aún no está aplicado; el sitio sigue usando el verde `accent-2`.

Contraste: el texto blanco sobre `#F26A1B` queda cerca de 3:1. Para texto pequeño sobre naranja usar `--color-accent-600` (`#cf530e`).

## Logo

`public/fotos/logo/`: `logo-orange.webp` (Nav y Footer), `logo-white.webp` (fondos naranja), `logo-black.jpg`.

## Favicon

Logo blanco sobre fondo naranja `#F26A1B`, generado desde `logo-white.webp`: `public/favicon.ico`, `favicon-32x32.png`, `favicon-16x16.png`, `apple-touch-icon.png` (180x180). Enlazados en `src/layouts/Layout.astro`. Si hay que regenerarlos, recortar el logo al área visible y centrarlo al 84% del lado del cuadrado.

## Tipografías (brandbook)

Amatic SC (títulos) y Calibri Light (cuerpo). El sitio usa hoy Caprasimo y Figtree (`--font-heading`, `--font-body`); no se han alineado.

## Equipo

Lista en `src/pages/nosotros.astro` (`equipo`). Fotos en `public/fotos/equipo/<slug>.webp`; con `photo: null` se muestran iniciales. Fotos nuevas: convertir a webp (`cwebp -q 80 -resize 0 1000`, ~1000 px de alto) con nombre en kebab-case y no dejar el JPEG original en `public/`. Todo el equipo ya tiene foto.

## Iconos

Los iconos en línea usan `currentColor` y heredan el naranja. Los 11 stickers `public/fotos/iconos/icono-01..11.webp` existen pero no se usan en el sitio.
