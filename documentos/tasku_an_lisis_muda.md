# UNIVERSIDAD MESOAMERICANA
**SEDE QUETZALTENANGO**  
**FACULTAD DE INGENIERÍA**  
**INGENIERÍA EN SISTEMAS, INFORMÁTICA Y CIENCIAS DE LA COMPUTACIÓN**

---

## EJEMPLO DE MUDA

**Integrantes:**
- Demy Brictany De León Figueroa
- Marco Pablo Siguenza Orozco
- Yordy Emmanuel Hernández Cabrera
- Juan José Efraín Martínez Delgado
- Adrian Pablo José Girón Franco

**QUETZALTENANGO, 02 DE NOVIEMBRE DE 2026**

---

# Análisis Muda aplicado a TaskU

## 1. Proyecto elegido
Aplicación móvil en Flutter para estudiantes universitarios de Quetzaltenango. Centraliza tareas, exámenes y proyectos; funciona sin Internet; modelo freemium con hasta 3 tareas activas gratis, publicidad AdMob y pase Premium de pago único con tableros grupales, nube, PDF y sin anuncios.

---

## 2. Ejemplo principal de Muda para TaskU

* **Desperdicio identificado:** Sobreproducción
* **Muda:** Construir funciones Premium y actividades de promoción demasiado amplias antes de validar el núcleo del MVP.
* **¿Dónde aparece?** En el alcance del proyecto: tableros grupales, sincronización en la nube, exportación a PDF, eliminación de anuncios, promoción en campus, redes sociales y varias líneas de crecimiento. Si el equipo intenta desarrollar todo eso antes de comprobar que el registro rápido, las alertas y el funcionamiento sin Internet realmente resuelven el problema de Diego, está produciendo más de lo que el cliente necesita en esta etapa.

### Clasificación entre los 7 desperdicios

| Muda | Aplicación en TaskU |
| :--- | :--- |
| **Sobreproducción** | Construir tableros, nube y PDF antes de validar el MVP. |
| **Puede derivar en Extraproceso** | Agregar campos o pasos innecesarios al registro de tareas, cuando la promesa es "registrar en segundos". |
| **Puede derivar en Defectos** | Más funciones sin validar = más bugs, retrabajo y carga para QA. |

### Evidencia de los documentos
* El sondeo sintético indica que el **66%** prioriza alertas o registro rápido.
* El **70%** olvida o entrega tarde actividades al menos ocasionalmente.
* El **74%** tiene cuatro o más pendientes por semana.
* Solo el **16%** considera suficiente el límite de 3 tareas gratis.
* El informe recomienda como MVP: registro de tareas en pocos pasos, alertas confiables y consulta sin conexión.
* Eso respalda no sobrecargar la primera versión con funciones Premium.

---

## 3. Cómo eliminar ese Muda

1. **Congelar el alcance del MVP:** registro rápido, recordatorios, funcionamiento offline y exportación manual JSON.
2. **Mover a fase 2 / Premium:** tableros grupales, respaldo automático en la nube, PDF y eliminación de anuncios.
3. **Usar los roles semanales para evitar retrabajo:**
   * **PM:** define criterios de aceptación.
   * **Arquitectura:** mantiene el repositorio y MVVM.
   * **UX:** valida flujo en pocos pasos.
   * **QA:** prueba casos límite.
   * **Release:** empaqueta solo lo aprobado.
4. **Probar el límite gratuito:** comparar 3 vs. 5 tareas activas antes de asumir que la barrera de 3 convierte bien.
5. **Medir con métricas reales:** tiempo para registrar una tarea, tareas registradas, retención, uso de alertas, llegada al límite y conversión efectiva a Premium.

---

## 4. Qué ganaría el cliente

### Diego Morales, estudiante universitario:
* Una app más simple y rápida, sin configuración compleja.
* Recordatorios confiables para no olvidar entregas.
* Acceso a pendientes sin Internet.
* Posibilidad de probar el valor real antes de pagar.
* Menos frustración por funciones que aún no necesita.

> **Ganancia para TaskU:** menor carga de desarrollo y QA, lanzamiento más rápido, menos bugs, mejor evidencia para decidir qué funciones Premium justifican el pago único.

---

## 5. Resumen listo para exponer

| Elemento | Respuesta |
| :--- | :--- |
| **Proyecto** | TaskU |
| **Muda identificado** | Sobreproducción |
| **Clasificación** | Producir más de lo necesario o antes de tiempo: construir funciones Premium antes de validar el MVP |
| **Evidencia** | El sondeo prioriza alertas, registro rápido y offline; el límite de 3 tareas genera fricción; el informe recomienda MVP simple |
| **Cómo eliminarlo** | Congelar MVP, mover tableros/nube/PDF a fase 2, validar 3 vs. 5 tareas y medir retención/conversión |
| **Ganancia para el cliente** | App más sencilla, útil desde el inicio, sin pasos innecesarios y con valor comprobable antes de pagar |

---

## 6. Otros Muda posibles en TaskU

| Muda | Ejemplo en TaskU | Cómo eliminarlo | Ganancia para el cliente |
| :--- | :--- | :--- | :--- |
| **Defectos** | Límite de 3 tareas gratis mal calibrado que provoca abandono. | Probar 3 vs. 5 tareas y ajustar según retención. | Experiencia gratuita más útil. |
| **Espera** | El usuario espera aprobación o pago para acceder a funciones básicas. | Mantener valor central gratis y dejar Premium para funciones avanzadas. | Empieza a organizarse sin fricción. |
| **Extraproceso** | Registro con demasiados campos obligatorios. | Registro en pocos toques; campos opcionales después. | Menos tiempo organizando. |
| **Transporte** | Usar varias apps o pasar información de cuaderno a celular. | Centralizar tareas, exámenes y proyectos en TaskU. | Toda la información en un solo lugar. |
| **Inventario** | Funciones o campañas listas que no se usan. | Lanzar solo lo validado y medir uso real. | Producto más enfocado. |
| **Movimiento** | Reuniones o cambios de alcance innecesarios. | Kanban semanal y criterios de aceptación claros. | Entregas más rápidas y estables. |
| **Sobreproducción** | Construir todo el Premium antes del MVP. | Fases: MVP $\rightarrow$ validación $\rightarrow$ Premium. | App simple y funcional desde el inicio. |