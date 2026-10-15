# Portafolio de Nicolás Ulloa Gatica

Sitio estático en Quarto. El portafolio presenta siete proyectos con páginas propias; los recursos educativos son una sección secundaria.

## Estructura

- `index.qmd`: presentación, perfil y tres proyectos destacados.
- `projects/index.qmd` y `projects/*/index.qmd`: catálogo con Listing nativo y siete fichas.
- `trayectoria.qmd`, `teaching/index.qmd`, `contacto.qmd`: experiencia, recursos y contacto.
- `assets/` y `downloads/`: imágenes reales, gráficos y las dos guías originales.
- `styles/`: tema grafito y verde petróleo, layout responsive y componentes.
- `docs/`: documentación de implementación, fuera del render.

La navegación, búsqueda, recursos y lista de fuentes renderizadas se definen en `_quarto.yml`. Inicio usa `page-layout: custom`; las demás páginas usan el layout de artículo de Quarto. Las fichas sin recurso visual se muestran como texto, sin miniatura de relleno. El avatar genérico de `assets/profile/` queda solo como respaldo no utilizado.

## Desarrollo local

```sh
quarto render
quarto preview
```

`_site/` es la salida estática para revisión o despliegue en GitHub Pages; `.quarto/` y `_site/` están ignorados por Git. No hay `site-url` porque aún no se ha elegido una URL de publicación. No se necesita servidor de aplicación.

Los cinco casos adicionales del paquete de entrega permanecen como borradores fuera del sitio activo. Su selección y aporte personal siguen sin precisarse.
