[README_DEPLOY.md](https://github.com/user-attachments/files/22993322/README_DEPLOY.md)
# Despliegue FIXO Demo

## Netlify (recomendado)
1. Inicia sesión en Netlify.
2. Crea un sitio desde Git: conecta tu repo de GitHub.
3. Nombre del sitio: `MANOSYO` (Netlify lo normaliza a minúsculas: `manosyo`).
4. Team: usa tu equipo con ID `68d55218ecf6d91394416f78`.
5. Publish directory: `web_demo`.
6. Deploy. URL público esperado: `https://manosyo.netlify.app/`.

Archivos ya preparados:
- `netlify.toml`: publica `web_demo` y añade fallback SPA.
- `robots.txt` y `sitemap.xml`: permiten indexación y SEO básicos.

## GitHub Pages
1. Crea el repo en GitHub: `fixo-demo`.
2. Sube el proyecto:
   ```bash
   git init
   git add .
   git commit -m "Deploy FIXO demo"
   git branch -M main
   git remote add origin https://github.com/alejandropm2004-ai/fixo-demo.git
   git push -u origin main
   ```
3. Activa Pages: Settings → Pages → Source: `Deploy from a branch`.
   - Branch: `main`, Folder: `/root`.
4. URL público: `https://alejandropm2004-ai.github.io/fixo-demo/`.

SEO:
- Edita `sitemap.xml` y reemplaza el dominio por el de producción si usas Pages.
- Meta `robots` y `description` ya insertadas en `index.html` y `fixo_simple.html`.

## Verificación en Google
- Añade el sitio en Google Search Console y envía `/sitemap.xml`.
- La indexación puede tardar desde minutos hasta días.
