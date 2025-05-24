# 🧠 Explicación de las consultas SQL

## 1. `SELECT * FROM animales;`

Muestra todas las filas y columnas de la tabla `animales`.

---

## 2. `SELECT * FROM animales WHERE id = 1;`

Devuelve los datos del animal cuyo `id` sea exactamente `1`.

---

## 3. `SELECT * FROM animales WHERE estado = "TRISTE" AND tipo = "GATITO";`

Busca animales que estén **tristes** y que sean del tipo **gatito**.  
Ambas condiciones deben cumplirse al mismo tiempo (`AND` lógico).

---

## 4. `UPDATE animales SET estado = "FURIOSO" WHERE id = 3;`

Modifica el valor del campo `estado` a `"FURIOSO"` únicamente para el registro con `id = 3`.

---

## 5. `SELECT * FROM animales;`

Se vuelve a consultar toda la tabla, probablemente para **verificar el cambio realizado** en el paso anterior.
