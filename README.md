# Misiles a Tierra — Sitio oficial

Sitio web estático de la banda de rock bogotana **Misiles a Tierra** (M.A.T.).

## Estructura

```
├── index.html          # Página principal
├── pages/              # Páginas internas
│   ├── bio.html
│   ├── discografia.html
│   ├── integrantes.html
│   ├── media.html
│   └── contacto.html
├── css/
│   └── style.css       # Hoja de estilos única (sin frameworks)
└── media/              # Imágenes y audio
```

## Cómo verlo localmente

Basta con abrir `index.html` en el navegador, o servirlo con:

```bash
npx serve .
# o
python3 -m http.server 8000
```

## Publicación en GitHub Pages

1. En el repositorio ve a **Settings → Pages**.
2. En *Source* elige la rama `main` y la carpeta `/ (root)`.
3. El sitio quedará en `https://<usuario>.github.io/<repo>/`.

## Formulario de contacto

El sitio es estático, así que el formulario necesita un servicio externo.
Crea una cuenta gratuita en [Formspree](https://formspree.io) y reemplaza
`TU_ID` en el atributo `action` de `pages/contacto.html`.

## Notas de la renovación (2026)

- Estructura de carpetas real (`css/`, `pages/`, `media/`) — antes los HTML
  apuntaban a rutas que no existían y el sitio se veía roto.
- Nombres de archivo en minúscula y sin tildes (`discografia.html`) para
  evitar problemas en servidores Linux y URLs.
- Se eliminó Bootstrap (se mezclaban las versiones 3 y 4 en la misma página)
  y jQuery; el sitio ahora usa solo CSS moderno (grid, scroll-snap).
- Se eliminaron ~30 archivos `bootstrap*.css/js` que estaban commiteados
  en la raíz sin usarse.
- HTML semántico y accesible: `alt` descriptivos, labels asociados,
  `prefers-reduced-motion`, foco visible.
- Carga diferida de imágenes (`loading="lazy"`) y audio (`preload="none"`).
