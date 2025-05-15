# Crear una Base de Datos y Tablas en SQL Server

[← Regresar al menú](../../README.md) <br>

Para crear una base de datos y tablas usando SQL Server. Este es el punto de partida fundamental para gestionar y consultar datos en cualquier sistema relacional.

---

## 🧠 Conceptos clave

- **Base de datos**: contenedor de todas tus tablas, procedimientos y datos.
- **Tabla**: estructura que almacena tus datos en filas (registros) y columnas (campos).
- **Tipos de datos**: definen el tipo de valor que una columna puede almacenar. Ej: `INT`, `VARCHAR`, `DATE`.

---

## 📌 Instrucciones básicas

### 1. Crear una base de datos
```sql
CREATE DATABASE TiendaVirtual;
GO
```

### 2. Seleccionar esa base de datos
```sql
USE TiendaVirtual;
GO
```

### 3. Crear una tabla
```sql
CREATE TABLE Clientes (
    ID INT PRIMARY KEY,
    Nombre VARCHAR(100) NOT NULL,
    Email VARCHAR(100),
    FechaRegistro DATE DEFAULT GETDATE()
);
```
### 4.Insertar datos
```sql
INSERT INTO Clientes (ID, Nombre, Email)
VALUES 
(1, 'Ana Ruiz', 'ana@email.com'),
(2, 'Luis Torres', 'luis@email.com'),
(3, 'Marta Chávez', NULL);
```

### 5. Visualización de datos
```sql
SELECT * FROM Clientes;
```
