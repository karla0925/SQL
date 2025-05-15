# Insertar, Actualizar y Eliminar Datos en SQL Server

[← Regresar al menú](../../README.md) <br>

Una vez creada una tabla, el siguiente paso es **manipular los datos** que contiene. Aquí aprenderás cómo insertar nuevos registros, modificarlos y eliminarlos con seguridad usando `INSERT`, `UPDATE` y `DELETE`.

---

## 🧠 Conceptos clave

- **INSERT**: agrega nuevas filas a una tabla.
- **UPDATE**: modifica datos existentes.
- **DELETE**: elimina filas de la tabla.

⚠️ Siempre usar `WHERE` con `UPDATE` o `DELETE` para evitar afectar todos los registros por error.

---

## 📌 Ejemplo práctico

Partimos de una tabla de ejemplo llamada `Clientes`:
```sql
CREATE TABLE Clientes (
    ID INT PRIMARY KEY,
    Nombre VARCHAR(100),
    Email VARCHAR(100),
    Ciudad VARCHAR(50)
);
```
## 1. Insertar registros
```sql
INSERT INTO Clientes (ID, Nombre, Email, Ciudad)
VALUES
(1, 'Ana Ruiz', 'ana@email.com', 'Lima'),
(2, 'Luis Torres', 'luis@email.com', 'Cusco'),
(3, 'Marta Chávez', NULL, 'Arequipa');
```
## 2. Actualizar registros existentes
Actualizar email de Marta
```sql
UPDATE Clientes
SET Email = 'marta@email.com'
WHERE ID = 3;
```
Cambiar ciudad de Luis
```sql
UPDATE Clientes
SET Ciudad = 'Trujillo'
WHERE Nombre = 'Luis Torres';
```
## 3. Eliminar registros
Eliminar a un cliente específico
```sql
DELETE FROM Clientes
WHERE ID = 2;
```
## Consultar después de los cambios
```sql
SELECT * FROM Clientes;
GO
```