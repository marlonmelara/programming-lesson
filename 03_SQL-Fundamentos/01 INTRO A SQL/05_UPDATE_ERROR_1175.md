
# 🧠 Explicación del `UPDATE` con error 1175

## 1. `UPDATE animales SET estado = "FURIOSO" WHERE tipo = "CHANCHITO";`

Intenta actualizar el campo `estado` a `"FURIOSO"` para todos los registros cuyo `tipo` sea `"CHANCHITO"`.

---

## ❌ Error mostrado: 1175

MySQL no permite ejecutar esta actualización porque estás en **modo seguro (safe update mode)** y la condición `WHERE` no incluye una **columna clave (como `id`)**.

Esto es para **evitar cambios accidentales masivos**.

---

## 💡 Soluciones posibles

1. Especificar la clave primaria en el `WHERE`, por ejemplo:

   ```sql
   WHERE id = 1
    ```

2. Desactivar el modo seguro temporalmente:

   ```sql
   SET SQL_SAFE_UPDATES = 0;
   ```

3. O permanentemente en MySQL Workbench:
   Ir a `Edit > Preferences > SQL Editor` y desmarcar **"Safe Updates"**, luego reconectar.

---
