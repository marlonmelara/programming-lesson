# 🧠 Explicación paso a paso del script `users`

## 🏗️ Creación de la tabla `users`

```sql
CREATE TABLE users (
    id INT NOT NULL AUTO_INCREMENT,
    name VARCHAR(50) NOT NULL,
    edad INT NOT NULL CHECK (edad > 0),
    email VARCHAR(100) NOT NULL UNIQUE,
    PRIMARY KEY (id)
);
```

* `id`: entero autoincremental y clave primaria.
* `name`: texto obligatorio, hasta 50 caracteres.
* `edad`: entero obligatorio, debe ser **positivo** (`CHECK (edad > 0)`).
* `email`: obligatorio y **único** (no se permite duplicados).

---

## 🧾 Inserción de registros

```sql
INSERT INTO users (...) VALUES (...);
```

Agrega 4 registros con valores válidos para todos los campos.

---

## 🔍 Consultas básicas

* `SELECT * FROM users;`: muestra todos los registros.
* `SELECT * FROM users LIMIT 1;`: devuelve solo la primera fila.

---

## 🔢 Consultas por condiciones numéricas

* `SELECT * FROM users WHERE edad > 15;`: mayores de 15 años.
* `SELECT * FROM users WHERE edad >= 15;`: 15 años o más.
* `SELECT * FROM users WHERE edad > 20 AND email = "nico@gmail.com";`: edad > 20 y correo exacto de Nico.
* `SELECT * FROM users WHERE edad > 20 OR email = "layla@gmail.com";`: uno u otro.

---

## ❗ Comparaciones y rangos

* `SELECT * FROM users WHERE email != "layla@gmail.com";`: todos menos Layla.
* `SELECT * FROM users WHERE edad BETWEEN 15 AND 30;`: edad entre 15 y 30 (ambos inclusive).

---

## 🔍 Búsqueda por patrones (`LIKE`)

* `LIKE "%gmail%"`: contiene “gmail” en cualquier parte.
* `LIKE "%gmail"`: termina en “gmail”.
* `LIKE "oscar%"`: comienza con “oscar”.

---

## 📊 Ordenamiento

* `ORDER BY edad ASC;`: orden ascendente por edad.
* `ORDER BY edad DESC;`: orden descendente.

---

## 🔢 Funciones de agregación

* `SELECT MAX(edad) AS mayor`: mayor edad registrada.
* `SELECT MIN(edad) AS mayor`: menor edad registrada (¡nombre del alias debería ser diferente!).

---

## 🎭 Selección parcial de columnas

* `SELECT id, name FROM users;`: solo muestra `id` y `name`.
* `SELECT id, name AS nombre FROM users;`: cambia el nombre de la columna `name` a `nombre` en el resultado.

---
