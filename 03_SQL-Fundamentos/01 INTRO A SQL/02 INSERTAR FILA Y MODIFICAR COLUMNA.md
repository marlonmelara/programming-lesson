# Insertar fila y modificar columna

## 🧠 Explicación del script

### 1. `INSERT INTO animales (tipo, estado) VALUES ('CHANCHITO','FELIZ');`

Inserta una fila en la tabla `animales` con los valores:

* `tipo`: "CHANCHITO"
* `estado`: "FELIZ"
  No se especifica `id` porque aún no es autoincremental.

---

### 2. `ALTER TABLE animales MODIFY COLUMN id INT AUTO_INCREMENT;`

Modifica la columna `id` para que sea **autoincremental**.
Esto permite que MySQL asigne automáticamente un valor único cada vez que se inserta un nuevo registro sin necesidad de especificarlo manualmente.
