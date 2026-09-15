# 🗄️ Proyecto Fundamentos Bases de datos SQL

## 📌 Título del Proyecto
**Análisis y Verificación de Bases de Datos Relacionales mediante Consultas SQL y CLI**

## 📝 Descripción General del Proyecto
Este proyecto está enfocado en la exploración, consulta y verificación funcional de bases de datos relacionales para una aplicación de transporte. La ejecución se lleva a cabo mediante comandos SQL en entorno de terminal Bash (Cygwin64), permitiendo extraer registros clave, auditar tablas operativas, filtrar códigos de error HTTP (`400` y `500`), procesar archivos de registro `.txt` y validar el conteo de datos para asegurar la integridad de la información del sistema backend.

---

## 🎯 Objetivos
* 📌 **Consulta y Filtrado Avanzado:** Implementar secuencias de comandos SQL para la adquisición rápida de datos esenciales desde múltiples tablas interrelacionadas.
* 📌 **Auditoría de Errores e Inconsistencias:** Identificar y extraer registros de fallos de servidor (errores `400 Bad Request` y `500 Internal Server Error`) redirigiéndolos a archivos `.txt` para análisis técnico.
* 📌 **Validación de Integridad de Datos:** Realizar operaciones de agregación (conteo total de registros, agrupaciones y análisis por periodos de tiempo) para contrastar el comportamiento de la plataforma de transporte.
* 📌 **Dominio de la Interfaz de Línea de Comandos (CLI):** Ejecutar flujos de trabajo eficientes desde la terminal para gestión y revisión directa de bases de datos sin interfaz gráfica.

---

## 📐 Alcance de las Pruebas
La verificación abarca la auditoría de esquemas de bases de datos y registros en servidores de la aplicación de transporte:

* 🗃️ **Estructura de la Base de Datos:** Verificación y cruce de información en más de 5 tablas relacionales (usuarios, viajes, vehículos, compañías y registros de tareas).
* 📊 **Consultas por Periodo Operativo:** Filtrado de métricas operativas especificadas por rangos de fecha y tiempo.
* 📑 **Auditoría de Logs e Incidentes:** Extracción y almacenamiento en directorios dedicados de solicitudes fallidas HTTP `400` y `500`.
* 🏢 **Listado de Compañías y Flotas:** Agrupación y clasificación de los proveedores de transporte registrados en el sistema.

---

## 🧪 Estrategia de Pruebas
La estrategia combina análisis estático de datos relacionales con ejecuciones de consultas dinámicas en la terminal:

1. 🔍 **Exploración de Esquemas:** Inspección inicial de claves primarias (`Primary Keys`), claves foráneas (`Foreign Keys`) y relaciones entre tablas.
2. ✍️ **Diseño e Interpretación de Consultas SQL:** Construcción de sentencias `SELECT`, `WHERE`, `JOIN`, `GROUP BY`, `COUNT` y filtros temporales para extraer muestras exactas de datos.
3. 💻 **Ejecución y Extracción vía CLI:**
   * Utilización del entorno de terminal **Cygwin64** para interactuar con la base de datos y el sistema de archivos del servidor.
   * Redirección de resultados y registros de error a directorios específicos en formato `.txt`.
4. ✅ **Aserción y Validación de Métricas:** Comprobación del número total de registros devueltos frente a los volúmenes esperados según las reglas del negocio.

---

## 🔬 Tipos de Pruebas
* 🗄️ **Pruebas de Base de Datos (Database Testing):** Validación de consistencia, duplicados y tipos de datos almacenados en las tablas.
* 💻 **Pruebas de Interfaz de Línea de Comandos (CLI Testing):** Evaluación del rendimiento y precisión de comandos ejecutados en la terminal Cygwin64.
* 📊 **Análisis y Extracción de Datos (Data Audit):** Agregación de registros para reportes operativos y análisis de métricas.
* 📑 **Análisis de Logs de Diagnóstico:** Identificación de errores de aplicación a través de la revisión de códigos de respuesta en registros del sistema.

---

## 🛠️ Herramientas y Tecnologías
* 🗃️ **Lenguaje de Consulta:** SQL (Structured Query Language)
* 🖥️ **Entorno de Terminal / CLI:** Cygwin64 Terminal
* 📊 **Gestión de Hojas de Cálculo:** Microsoft Excel / Google Sheets
* 📄 **Procesamiento de Documentos y Evidencias:** Google Docs / Hojas de Texto

---

## 📋 Casos de Prueba
Se diseñaron e implementaron diversos scripts y consultas SQL para validar la información contenida en el sistema:

| ID Caso | Descripción de la Prueba / Consulta | Herramienta | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **TC-SQL-01** | Conteo total de registros en la tabla de viajes | SQL / Cygwin64 | Cantidad exacta de filas retornada correctamente. |
| **TC-SQL-02** | Filtrado e identificación de compañías registradas | SQL | Lista completa de compañías asociadas sin duplicados. |
| **TC-SQL-03** | Consulta de datos filtrada por periodo temporal específico | SQL | Registros delimitados dentro del rango de fechas definido. |
| **TC-SQL-04** | Cruce de datos entre más de 5 tablas relacionales | SQL (`JOIN`) | Tablas combinadas asociando correctamente las relaciones de la app. |
| **TC-SQL-05** | Creación de directorio local para almacenamiento de errores | Bash CLI | Directorio creado en la ruta definida mediante comandos de terminal. |
| **TC-SQL-06** | Extracción e impresión de errores HTTP `400` y `500` en `.txt` | CLI / SQL | Registro de logs de fallas exportado exitosamente a un archivo de texto. |

---

## 🐛 Reporte de Defectos
Durante el proceso de auditoría mediante terminal y SQL, se categorizaron los hallazgos según su origen:

* 🚨 **Logs de Error HTTP 500 (Internal Server Error):** Detección de peticiones con fallas críticas del lado del servidor registradas en los archivos de eventos.
* ⚠️ **Logs de Error HTTP 400 (Bad Request):** Identificación de solicitudes malformadas o parámetros no válidos enviados a la base de datos.
* 📊 **Inconsistencias en Registros:** Hallazgo de datos desactualizados o faltantes en tablas de asignación de tareas operativas.

---

## 📊 Resultados y Métricas
* 🗃️ **Tablas Auditadas:** +5 tablas relacionales analizadas e interconectadas.
* 📜 **Scripts y Consultas Ejecutadas:** Múltiples sentencias SQL complejas probadas en la terminal.
* 📑 **Archivos de Reporte Generados:** Registros de errores `400` y `500` extraídos e integrados en directorios específicos para el equipo de desarrollo.
* ✅ **Resultado del Proyecto:** Verificación exitosa de los datos de la aplicación de transporte, facilitando la detección de inconsistencias backend e impulsando la calidad del sistema.

---

## 📂 Evidencias
* 📄 **Documentación Técnica del Proyecto SQL:** [Ver Documento de Evidencias de Base de Datos en Google Docs](https://docs.google.com/document/d/1UJamzI5ltx3QeYSgMkHLeHhfiTFIBqWp/edit?usp=sharing&ouid=117662769631159222767&rtpof=true&sd=true)

---

## 📁 Estructura del Repositorio
```text
sql-database-fundamentals/
├── scripts/
│   ├── count_records.sql       # Consultas de conteo y agregación de datos
│   ├── filter_by_period.sql    # Consultas filtradas por fecha/periodo
│   └── join_companies.sql      # Cruce relacional de tablas de la aplicación
├── logs/
│   ├── error_400_logs.txt      # Registros extraídos con códigos HTTP 400
│   └── error_500_logs.txt      # Registros extraídos con códigos HTTP 500
├── docs/
│   └── sql_findings_report.pdf # Reporte consolidado de hallazgos
└── README.md                   # Documentación general del proyecto
```

---

## 💡 Principales Aprendizajes
* 🧠 **Dominio de Sintaxis SQL:** Construcción eficiente de consultas para agregación, filtrado por fechas y combinación de tablas múltiples.
* 🖥️ **Manejo Profesional de Terminal (CLI):** Uso efectivo de **Cygwin64** para la navegación de directorios, procesamiento de archivos y manejo de cadenas de comandos.
* 📑 **Gestión de Registros de Error:** Extracción automatizada y redirigida de archivos `.txt` para aislar fallos del servidor HTTP `400` y `500`.
* 📊 **Análisis Relacional:** Comprensión profunda de la arquitectura de datos detrás de una plataforma de servicios de transporte.

---

## 🚀 Mejoras Futuras
* ⚙️ **Automatización de Scripts Bash:** Crear scripts ejecutables `.sh` que automaticen la extracción de logs de error de forma periódica.
* 📈 **Optimización de Consultas SQL:** Aplicar índices en las columnas de mayor consulta (fechas e identificadores) para reducir tiempos de respuesta.
* 📊 **Integración con Herramientas de BI:** Conectar la base de datos a herramientas como Power BI o Tableau para generar tableros visuales de métricas.