# TaskU · Estrategia y validación

Dossier web del proyecto **TaskU**, una aplicación móvil en Flutter para el seguimiento de tareas, exámenes y proyectos académicos universitarios. Reúne los cinco documentos del proyecto y añade un diagnóstico estratégico con matrices EFI, EFE y análisis PESTEL.

**Sitio publicado:** https://jjemd101191.github.io/tasku-estrategia/

## Contenido

| # | Sección | Origen |
| :-: | :--- | :--- |
| 01 | Proyecto y propuesta de valor | `documentos/documento_del_proyecto_tasku.md` |
| 02 | Business Model Canvas | `documentos/business_model_canvas_tasku.md` |
| 03 | Matriz de Perfil Competitivo | `documentos/matriz_de_perfil_competitivo_tasku.md` |
| 04 | Matriz EFI | Análisis agregado |
| 05 | Matriz EFE | Análisis agregado |
| 06 | Análisis PESTEL | Análisis agregado |
| 07 | Análisis Muda | `documentos/tasku_an_lisis_muda.md` |
| 08 | Sondeo de productividad académica | `documentos/informe_de_sondeo_simulado_tasku.md` |

## Análisis agregados

- **EFI (2.85 / 4.00):** once factores internos ponderados. Fortalezas en especialización académica, simplicidad y operación offline; debilidades críticas en marca y en el límite de tres tareas gratuitas.
- **EFE (2.79 / 4.00):** trece factores externos. La demanda declarada y la intención de uso son la oportunidad principal; la competencia gratuita consolidada y la sensibilidad al precio son las amenazas mayores.
- **PESTEL:** lectura de las dimensiones política, económica, social, tecnológica, ecológica y legal, con su efecto e intensidad sobre el proyecto.
- **Lectura integrada:** con EFI y EFE por encima de 2.50, TaskU se ubica en el cuadrante de *crecer y construir* de la matriz IE. El resultado habilita validación y foco, no afirma viabilidad comercial.

## Estructura

```text
.
├── index.html              Página completa, autocontenida (CSS y JS inline)
├── documentos/             Cinco documentos fuente en Markdown
├── docs/BITACORA.md        Bitácora de sesiones
├── .nojekyll               Evita el procesamiento de Jekyll en GitHub Pages
└── README.md
```

## Ver localmente

Abre `index.html` en el navegador o sirve la carpeta:

```bash
npx serve .
```

## Notas metodológicas

- El sondeo se aplicó a **50 perfiles sintéticos**. Sus porcentajes son ilustrativos y no prueban adopción, conversión ni viabilidad comercial.
- Las calificaciones de la Matriz de Perfil Competitivo son estimaciones académicas. Las tablas detalladas suman TaskU 3.45, Microsoft To Do 3.35, Google 3.20, Trello 3.05 y Notion 2.95; el resumen del documento original cita otros totales. La página usa los totales reproducibles de la matriz detallada y lo advierte.
- Los pesos y calificaciones de EFI, EFE y PESTEL fueron construidos a partir de la evidencia de los cinco documentos. No son mediciones de mercado.
- La página no usa librerías externas de JavaScript. Solo carga las tipografías Inter e Instrument Serif desde Google Fonts.

## Equipo

Demy Brictany De León Figueroa · Marco Pablo Siguenza Orozco · Yordy Emmanuel Hernández Cabrera · Juan José Efraín Martínez Delgado · Adrian Pablo José Girón Franco

Universidad Mesoamericana, sede Quetzaltenango · Ingeniería en Sistemas · Noviembre de 2026.

## Versión

**1.0.0** · primera publicación · 2026-11-04
