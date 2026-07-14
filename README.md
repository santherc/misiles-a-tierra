# Misiles a Tierra — Sitio oficial

Sitio web estático de la banda de rock bogotana **Misiles a Tierra** (M.A.T.).

## Estructura

Todos los archivos viven en la raíz del repositorio: las páginas HTML
(`index.html`, `bio.html`, `discografia.html`, `integrantes.html`,
`media.html`, `contacto.html`), la hoja de estilos `style.css` y los
archivos de imagen y audio.

## Cómo verlo localmente

Basta con abrir `index.html` en el navegador.

## Publicación en GitHub Pages

1. En el repositorio ve a **Settings → Pages**.
2. En *Source* elige la rama `main` y la carpeta `/ (root)`.
3. El sitio quedará en `https://<usuario>.github.io/<repo>/`.

## Formulario de contacto

El sitio es estático, así que el formulario necesita un servicio externo.
Crea una cuenta gratuita en [Formspree](https://formspree.io) y reemplaza
`TU_ID` en el atributo `action` de `contacto.html`.

## Notas de la renovación (2026)

- Se eliminó Bootstrap (se mezclaban las versiones 3 y 4) y jQuery;
  el sitio usa solo CSS moderno (grid, scroll-snap).
- Nombres de archivo en minúscula y sin tildes para evitar problemas
  en servidores Linux y URLs.
- HTML semántico y accesible: `alt` descriptivos, labels asociados,
  `prefers-reduced-motion`, foco visible.
- Carga diferida de imágenes (`loading="lazy"`) y audio (`preload="none"`).
