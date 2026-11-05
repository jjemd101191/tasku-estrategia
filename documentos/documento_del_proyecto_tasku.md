# Resumen del proyecto: TaskU

**TaskU** es una aplicación móvil desarrollada en Flutter para el seguimiento estructurado de compromisos académicos (tareas, exámenes y proyectos). Nace de un problema concreto: en la universidad, las entregas y los exámenes se pierden entre horarios dispersos, libretas sin automatización y herramientas genéricas (Notion, ClickUp) con una curva de aprendizaje demasiado alta para la dinámica ágil de un estudiante.

Su viabilidad económica se resuelve con un modelo híbrido: publicidad pasiva (AdMob) en la versión gratuita y un esquema freemium con una barrera de 3 tareas activas simultáneas que motiva la compra de un pase Premium accesible, con pago único.

---

## Versiones del producto

| Característica | Estudiante Estándar (Gratis) | Estudiante Premium (Pro) |
| :--- | :--- | :--- |
| **Tareas** | Hasta 3 activas simultáneas | Ilimitadas, con recordatorios |
| **Proyectos** | No disponible | Tableros de proyectos grupales |
| **Datos** | Almacenamiento local y exportación manual (JSON) | Sincronización y respaldo automático en la nube |
| **Publicidad** | Banners AdMob | Sin publicidad |
| **Exportación** | Archivo de respaldo | Exportación a PDF |

> **Nota técnica:** Además existe el rol **Administrador del Sistema** (configuración de umbrales y tarifas, auditoría de errores y métricas, respaldo central), que no es cliente sino supervisor técnico.

---

## 1. User Persona

Se construyó una persona principal, correspondiente al usuario que descargará la versión gratuita y que, con el tiempo, puede convertirse en Premium.

### Perfil Principal: Diego Morales

* **Edad:** 21 años
* **Ocupación:** Estudiante universitario ($5.^\circ - 8.^\circ$ semestre)
* **Dispositivo:** Smartphone como principal herramienta de consulta
* **Nivel tecnológico:** Básico / intermedio
* **Cita textual:** *"Tengo muchos cursos, entregas y trabajos en equipo, y a veces se me pasa algo. Quiero una app sencilla, no otra herramienta pesada que aprender."*

#### Objetivos
* Mantener organizadas tareas y exámenes.
* No olvidar entregas ni fechas importantes.
* Tener toda su información académica en un solo lugar.
* Coordinar proyectos y trabajos grupales.
* Consultar pendientes rápido desde el celular.

#### Frustraciones
* Horarios y fechas dispersos en varias plataformas.
* Libretas y blocs de notas sin recordatorios activos.
* Herramientas como Notion o ClickUp: complejas de configurar y mantener.
* Usar varias aplicaciones distintas a la vez.
* Dificultad para coordinar equipos de trabajo.

#### Necesidades
* Una aplicación sencilla, con registro de tareas en pocos toques.
* Recordatorios de entregas y exámenes confiables.
* Acceso sin conexión a sus pendientes.
* Respaldo seguro de la información.
* Herramientas prácticas para proyectos grupales.

#### Comportamiento habitual
* Consulta sus pendientes principalmente desde el teléfono.
* Busca soluciones rápidas y fáciles de usar; abandona lo que exige demasiada configuración previa.
* Empieza con una aplicación gratuita y solo paga si comprueba que le es útil y necesita más capacidad.

#### Motivaciones para pasar a Premium
* Tener tareas ilimitadas cuando aumenta la carga del semestre.
* Trabajar en proyectos grupales con tableros compartidos.
* No perder información al cambiar de dispositivo (respaldo automático en la nube).
* Eliminar por completo la publicidad.
* Exportar su información académica a PDF.

---

### Persona secundaria: Estudiante Premium (Pro)
Estudiante con alta carga de cursos o proyectos en equipo (por ejemplo, el mismo Diego durante un semestre especialmente exigente). Su disparador de compra es llegar a la cuarta tarea activa o necesitar un tablero grupal coordinado.

---

## 2. Lienzo de Propuesta de Valor

El lienzo conecta las necesidades del estudiante (perfil del cliente) con las características del producto (mapa de valor).

```
+--------------------------------------------------+     +--------------------------------------------------+
|               MAPA DE VALOR (TaskU)              |     |       PERFIL DEL CLIENTE (Diego, estudiante)     |
+--------------------------------------------------+     +--------------------------------------------------+
| PRODUCTOS Y SERVICIOS:                           |     | TRABAJOS DEL CLIENTE:                            |
| • App móvil en Flutter                           |     | • Registrar tareas y exámenes                    |
| • Registro rápido de tareas y exámenes           |     | • Recordar fechas de entrega                     |
| • Recordatorios y alertas                        |     | • Dar seguimiento a pendientes                   |
| • Almacenamiento local (SQLite / Hive)           |     | • Coordinar trabajos grupales                    |
| • Respaldo manual en JSON                        |     | • Mantener respaldada su información             |
| • Tableros de proyectos grupales                 |     +--------------------------------------------------+
| • Sincronización en la nube                      |     | DOLORES (Pains):                                 |
| • Exportación a PDF                              |     | • Olvidar entregas y exámenes                    |
| • Modalidades Gratis y Premium                   |     | • Información dispersa                           |
|                                                  |     | • Herramientas complejas                         |
| CREADORES DE GANANCIAS:                          |     | • Pérdida de datos al cambiar de equipo          |
| • Todo lo académico en un solo lugar             |     | • Difícil coordinación de grupos                 |
| • Consulta sin Internet                          |     +--------------------------------------------------+
| • Interfaz simple (registro en segundos)         |     | GANANCIAS (Gains):                               |
| • Trabajo grupal coordinado                      |     | • Mayor organización personal                    |
| • Datos protegidos en la nube                    |     | • Menos olvidos y entregas a tiempo              |
| • Experiencia sin anuncios (Premium)             |     | • Acceso rápido desde el celular                 |
|                                                  |     | • Información disponible offline                 |
| ALIVIADORES DE DOLORES:                          |     | • Mejor coordinación con compañeros              |
| • Recordatorios evitan olvidos                   |     +--------------------------------------------------+
| • Centraliza fechas y horarios                   |
| • Curva de aprendizaje mínima                    |
| • Respaldo y sincronización                      |
| • Tableros colaborativos                         |
+--------------------------------------------------+
```

### Tabla de ajuste: Dolor vs. Solución

| Dolor del cliente | Cómo lo resuelve TaskU |
| :--- | :--- |
| **Olvidar entregas y exámenes** | Registro rápido de tareas y alertas/recordatorios confiables. |
| **Información dispersa** | Centralización de tareas, exámenes y proyectos en una sola app. |
| **Herramientas complicadas** | Interfaz enfocada en estudiantes, con curva de aprendizaje mínima. |
| **Falta de conexión constante** | Persistencia local (SQLite / Hive): funciona 100 % sin Internet. |
| **Pérdida de información** | Respaldo manual en JSON (gratis) y sincronización automática en la nube (Premium). |
| **Dificultad en trabajos grupales** | Tableros de proyectos colaborativos en tiempo real (Premium). |

### Declaración de Propuesta de Valor
> **TaskU** es una aplicación móvil para estudiantes universitarios que centraliza tareas, exámenes y proyectos académicos en una herramienta sencilla, permitiendo organizar los compromisos en segundos y consultarlos incluso sin conexión.
>
> **Eslogan:** *"TaskU: menos tiempo organizando, más tiempo estudiando."*

---

## 3. Business Model Canvas

### Detalle de los nueve bloques

| Bloque | Detalle en TaskU |
| :--- | :--- |
| **Segmentos de clientes** | Estudiantes universitarios con varios cursos, tareas y proyectos grupales. Nicho de conversión: estudiantes con alta carga académica (perfil Premium). |
| **Propuesta de valor** | App académica sencilla que centraliza tareas, exámenes y proyectos; funciona sin conexión; gratuita para empezar y Premium para escalar. |
| **Canales** | App móvil distribuida en tiendas (Google Play / App Store); redes sociales; promoción en campus y comunidades estudiantiles; recomendación boca a boca entre compañeros. |
| **Relación con clientes** | Autoservicio dentro de la app; conversión progresiva de Gratis a Premium mediante un modal de actualización al intentar registrar una cuarta tarea o crear un tablero grupal; soporte por correo y FAQ. |
| **Fuentes de ingresos** | Publicidad AdMob (banners en versión gratuita) y cobro de pago único por el pase Premium accesible. |
| **Recursos clave** | Aplicación Flutter (arquitectura MVVM), base de datos local, infraestructura en la nube, sistema de cuentas / estado `isPremium` y equipo de desarrollo. |
| **Actividades clave** | Desarrollo y mantenimiento de software, sincronización y respaldo de datos, gestión de cuentas y pagos Premium, análisis de métricas de uso y corrección de errores. |
| **Socios clave** | Proveedores cloud (Firebase / AWS), plataformas de publicidad móvil (Google AdMob), tiendas de aplicaciones (Play Store / App Store), pasarelas de pago y universidades/comunidades estudiantiles locales. |
| **Estructura de costos** | Horas de desarrollo y mantenimiento, infraestructura cloud (almacenamiento y sincronización), comisiones de tiendas de aplicaciones (15-30 %), marketing universitario, soporte y administración técnica. |

---

## 4. Modelo de ingresos y embudo de conversión

### Embudo de conversión Freemium $\rightarrow$ Premium

```
[ 1. Descarga gratuita ]
  • Instala TaskU y registra tareas iniciales.
  • Monetización pasiva: Banners AdMob.
             │
             ▼
[ 2. Uso habitual ]
  • Hasta 3 tareas activas simultáneas.
  • Datos locales + respaldo manual en JSON.
             │
             ▼
[ 3. Barrera Freemium ]
  • El estudiante intenta agregar una 4.ª tarea o crear un tablero grupal.
  • Se despliega el modal de actualización a Premium.
             │
             ▼
[ 4. Premium (Conversión) ]
  • Pago único accesible.
  • Habilita tareas ilimitadas, tableros grupales, nube, PDF y retira anuncios.
```

**Mecánica de conversión:**
La conversión ocurre de forma orgánica cuando el estudiante llega a su cuarta tarea activa en el ciclo semanal o intenta crear un tablero grupal con compañeros. En la versión de prueba o desarrollo, el flujo activa un modal con pago único simulado que conmuta el estado de la cuenta (`isPremium = true`), desbloqueando de inmediato tareas ilimitadas, respaldo en la nube y eliminando la publicidad de AdMob.