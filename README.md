# ECOWATT – Sitio estático listo para GitHub/Netlify

Este paquete contiene **`index.html`** y **placeholders** para **todas las rutas de assets** referenciadas (imágenes, íconos, videos y PDFs) para evitar 404 al desplegar. Reemplace cada placeholder por el archivo real **manteniendo exactamente el mismo nombre y ruta**.

## Estructura
```
.
├─ index.html
├─ Ecowatt_general.pdf
├─ 2G_catalogo.pdf
├─ assets/
│  ├─ logos/
│  │  ├─ ecowatt.png
│  │  └─ partners/
│  │     ├─ 2g.png
│  │     ├─ airclean.png
│  │     ├─ aqana.png
│  │     ├─ daga.png
│  │     └─ fuchs.png
│  ├─ icons/
│  │  ├─ agitador-blue (2).svg
│  │  ├─ aire-blue (2).svg
│  │  ├─ cloaca-blue (2).svg
│  │  └─ gota-blue (2).svg
│  ├─ img/
│  │  └─ hero/hero-ecowatt.jpg
│  ├─ videos/hero.mp4
│  └─ gallery/
│     ├─ group1/img1.jpg … img6.jpg
│     ├─ group2/img1.jpg … img6.jpg
│     └─ group3/img1.jpg … img6.jpg
```

> **Nota**: Todos esos archivos existen como **placeholders** (PNG/SVG/PDF/MP4 vacíos o mínimos). Sustitúyalos por los reales cuando los tenga.

## Cómo publicar en GitHub Pages (sin builds)
1. Cree un repositorio nuevo en GitHub (p. ej. `ecowatt-site`).
2. Suba **todo el contenido** de esta carpeta a la rama `main` (arrastrar y soltar o `git push`).
3. En **Settings → Pages**:
   - *Source*: `Deploy from a branch`
   - *Branch*: `main` / root (`/`)
4. Guarde. La URL pública aparecerá arriba (tarda 1–2 minutos).

## Cómo publicar en Netlify
1. Ingrese a Netlify y elija **Add new site → Import an existing project**.
2. Conecte con GitHub y seleccione su repo.
3. **Build command**: _(vacío)_ – No se requiere build.
4. **Publish directory**: `/` (root).
5. Deploy. La URL estará activa al finalizar.

## Verificaciones rápidas (QA)
- **Header**: logo +20% y `Descargas` (dropdown accesible) ubicado a la **izquierda** de `Consultar`.
- **Hero**: tarjeta alineada a la izquierda (gutter común), sin invadir la banda siguiente.
- **Soluciones y tecnologías**: primer `h4` azul, el resto verdes; botones `saber más…` a la derecha y a la misma altura.
- **Galería**: visor 1:1 (≈378×378px); en móvil, miniaturas ocultas y controles `‹` `›` visibles.
- **Partners**: links correctos; logos en línea con altura ≤ logo Ecowatt.
- **Contacto**: 2 columnas en desktop, apilado en móvil.
- **Placeholders**: todos presentes; al sustituir, respete **nombre y ruta** exactos.

## Desarrollo local
- Basta con abrir `index.html` en su navegador.
- Si usa Live Server / http-server, no requiere configuración adicional.

## Accesibilidad y responsivo
- Dropdown y modales manejan **tabfocus** y **Escape**.
- Validado en anchos **≥1200, 992, 768, 576 y 360 px**.

---
**ECOWATT – Ingeniería ambiental aplicada**  
Cualquier duda: actualice el issue de despliegue en su repo.
