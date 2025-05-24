# 🧠 Explicación de las sentencias y el resultado

## 1. `DELETE FROM animales WHERE estado = "FURIOSO";`

Intenta eliminar los registros donde el estado sea `"FURIOSO"`.  
❗ **Error mostrado:**  
MySQL está en **Safe Update Mode**, que impide ejecutar `DELETE` o `UPDATE` si no usas una condición con una **clave primaria** (como `id`). Esto es una medida de seguridad para evitar borrar datos por error.

---

## 2. Comentarios del error (líneas 39–42)

Explican por qué ocurrió el error:

- No se puede ejecutar DELETE sin una condición con clave (`KEY column`) si está activo el modo seguro.
- Sugiere desactivarlo desde `Preferences -> SQL Editor`.

---

## 3. `DELETE FROM animales WHERE id = 3;`

Esta sentencia sí es válida, ya que usa una condición con la columna clave primaria (`id`).
🗑️ Elimina el registro con `id = 3`.

---

## 4. `SELECT * FROM animales;`

Consulta para ver el estado actual de la tabla después de la eliminación.

---

## 🧾 Resultado en la tabla (grilla inferior)

La fila con `id = 3` ya no aparece.  
Los registros restantes son:

| id | tipo      | estado  |
|----|-----------|---------|
| 1  | CHANCHITO | FELIZ   |
| 2  | CHANCHITO | ENOJADO |
| 4  | CHANCHITO | TRISTE  |
| 5  | GATITO    | TRISTE  |
