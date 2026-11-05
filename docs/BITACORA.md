# Bitácora — TaskU · Estrategia y validación

## 2026-11-04 · Sesión 2 · Ajuste de contraste en tema oscuro

- **Objetivo:** corregir el contraste del monograma, el avatar y el icono de advertencia en tema oscuro.
- **Rama:** `main`.
- **Hecho en esta sesión:**
  - Se añadieron los tokens `--brand-ink` y `--warning-ink` con valores distintos por tema.
  - El monograma y el avatar usan tinta oscura sobre el acento claro en modo oscuro.
- **Archivos tocados:** `index.html`, `README.md`, `docs/BITACORA.md`.
- **Verificación:** captura Edge headless del encabezado en tema oscuro → monograma legible; sin errores de consola.
- **Versión:** PATCH → `1.0.1` — corrección visual compatible.
- **Commits/PR:** ver `git log`.
- **Pendiente / siguiente paso:** comprobar la versión desplegada en GitHub Pages.
- **Decisiones o riesgos:** los tokens permiten ajustar el contraste sin duplicar reglas por componente.

## 2026-11-04 · Sesión 1 · Publicación del dossier estratégico

- **Objetivo:** convertir los cinco documentos Markdown de TaskU en una página web navegable, agregar matrices EFI/EFE y análisis PESTEL, y publicarla en GitHub Pages.
- **Rama:** `main`.
- **Hecho en esta sesión:**
  - Se construyó `index.html` como página autocontenida con ocho secciones desplegables, navegación, tema claro/oscuro, modo responsive y doce gráficos de barras para el sondeo.
  - Se integraron los cinco documentos fuente sin recortar su contenido sustantivo.
  - Se agregaron la Matriz EFI (2.85 / 4.00), la Matriz EFE (2.79 / 4.00), el análisis PESTEL y una lectura estratégica integrada.
  - Se documentó la inconsistencia de totales de la Matriz de Perfil Competitivo y se usaron los totales reproducibles de la tabla detallada.
- **Archivos tocados:** `index.html`, `README.md`, `docs/BITACORA.md`, `documentos/*.md`, `.nojekyll`.
- **Verificación:** renderizado con Edge headless en 1440 px y 390 px, en tema claro y oscuro → sin errores de consola; revisión visual de hero, canvas, matriz competitiva, EFI, PESTEL y sondeo. Pendiente de verificación: Firefox y Safari.
- **Versión:** `1.0.0` — primera publicación del sitio.
- **Commits/PR:** commit inicial de esta sesión.
- **Pendiente / siguiente paso:** activar GitHub Pages y comprobar la URL pública; validar la página en otros navegadores.
- **Decisiones o riesgos:** las cifras del sondeo son sintéticas y los pesos de EFI/EFE/PESTEL son estimaciones académicas; la página lo advierte en cada sección. El contenido incluye los nombres del equipo, presentes en el documento original.
