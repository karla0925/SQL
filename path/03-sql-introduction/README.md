# Introducción a SQL Server

[← Regresar al menú](../../README.md) <br>

---

## ¿Qué es SQL Server?

**SQL Server** es un sistema de gestión de bases de datos relacional (RDBMS) desarrollado por Microsoft. Está diseñado para almacenar, administrar y recuperar datos mediante el lenguaje SQL (Structured Query Language).

Como analista de datos, SQL Server te permite acceder, transformar y analizar grandes volúmenes de información de forma rápida y estructurada. Es ampliamente usado en entornos empresariales, financieros, de salud y comercio electrónico.

---

## ¿Por qué aprender SQL Server?

Aprender SQL Server es clave para trabajar como analista de datos por estas razones:

- 🔍 Permite ejecutar consultas complejas sobre grandes volúmenes de datos.
- 🛠️ Facilita tareas de limpieza, transformación y validación de datos.
- 📊 Se integra con herramientas como Power BI, Excel y aplicaciones de desarrollo.
- 💼 Es uno de los RDBMS más solicitados en ofertas laborales de análisis de datos.

---

## Características clave

- Lenguaje estándar: usa **Transact-SQL (T-SQL)**.
- Interfaz gráfica amigable: **SQL Server Management Studio (SSMS)**.
- Alta seguridad en la gestión de datos.
- Permite programar procedimientos, funciones, vistas, y triggers.
- Soporte para integraciones con Python, R y Power BI.

---

## Estructura básica en SQL Server

- **Servidor**: el motor de base de datos que ejecuta las consultas.
- **Base de datos (Database)**: contenedor lógico de todas las tablas y objetos.
- **Tabla (Table)**: conjunto estructurado de datos.
- **Fila (Row)**: cada registro de una tabla.
- **Columna (Column)**: cada campo de un registro.

---
# Tipos de Datos en SQL Server

En SQL Server, cada columna de una tabla debe tener un tipo de dato que defina el tipo de valor que puede almacenar. Esta guía resume los tipos más comunes que usarás como analista de datos.

---

## 📌 Tipos Numéricos

| Tipo de dato      | Descripción                                          | Ejemplo de uso        |
|-------------------|------------------------------------------------------|------------------------|
| `INT`             | Entero grande (±2 mil millones)                      | Edad, ID               |
| `BIGINT`          | Entero más grande (±9 quintillones)                  | IDs masivos            |
| `SMALLINT`        | Entero pequeño (±32,767)                             | Cantidad pequeña       |
| `TINYINT`         | Entero de 0 a 255                                    | Estado, nivel          |
| `DECIMAL(p, s)`   | Número fijo con precisión y escala                   | Precio: `DECIMAL(10,2)`|
| `FLOAT`           | Número con punto flotante (aproximado)              | Temperatura, mediciones|
| `BIT`             | Booleano: 1 (true), 0 (false)                        | ¿Está activo?          |

---

## 📌 Tipos de Texto

| Tipo de dato      | Descripción                                          | Ejemplo de uso        |
|-------------------|------------------------------------------------------|------------------------|
| `CHAR(n)`         | Texto fijo de n caracteres                          | Código postal          |
| `VARCHAR(n)`      | Texto variable de hasta n caracteres                | Nombre, email          |
| `VARCHAR(MAX)`    | Texto largo (hasta 2GB)                             | Comentarios, reseñas   |


---

## 📌 Tipos de Fecha y Hora

| Tipo de dato      | Descripción                                          | Ejemplo de uso        |
|-------------------|------------------------------------------------------|------------------------|
| `DATE`            | Solo fecha (YYYY-MM-DD)                             | Fecha de nacimiento    |
| `TIME`            | Solo hora (hh:mm:ss)                                | Hora de ingreso        |
| `DATETIME`        | Fecha y hora combinadas                             | Registro de compra     |
| `DATETIME2`       | Mayor precisión que `DATETIME`                      | Logs detallados        |
| `SMALLDATETIME`   | Precisión más baja que `DATETIME`                   | Tiempos de eventos     |

---

## 📌 Otros tipos útiles

| Tipo de dato           | Descripción                                           | Ejemplo de uso          |
|------------------------|-------------------------------------------------------|--------------------------|
| `UNIQUEIDENTIFIER`     | Identificador global único (GUID)                    | ID alternativo           |
| `BINARY` / `VARBINARY` | Datos binarios (imágenes, archivos)                  | Archivos adjuntos        |
| `XML`                  | Datos en formato XML                                 | Estructura compleja      |
| `JSON` *(via NVARCHAR)*| Se guarda como texto usando `NVARCHAR`               | Respuestas API, config.  |

---

## ✅ Recomendaciones para analistas de datos

| Caso de uso           | Tipo recomendado          |
|------------------------|---------------------------|
| ID de usuario          | `INT` o `BIGINT` + `PRIMARY KEY` |
| Nombre, email          | `VARCHAR(100)`            |
| Fecha de registro      | `DATETIME`                |
| Precio / Monto         | `DECIMAL(10,2)`           |
| Estado (activo/inactivo)| `BIT`                    |
