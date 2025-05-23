
# 🐘 Scripts básicos en MySQL

## 🔹 Crear una base de datos

```sql
CREATE DATABASE holamundo;
```

* **Crea** una base de datos llamada `holamundo`.

---

## 🔹 Seleccionar la base de datos

```sql
USE holamundo;
```

* **Selecciona** la base de datos `holamundo` para trabajar con ella.

---

## 🔹 Crear una tabla

```sql
CREATE TABLE animales (
  id INT,
  tipo VARCHAR(255),
  estado VARCHAR(255),
  PRIMARY KEY (id)
);
```

### 📋 Estructura de la tabla `animales`

1. `id INT`: Identificador numérico único.
2. `tipo VARCHAR(255)`: Tipo de animal (ej. "gato", "perro").
3. `estado VARCHAR(255)`: Estado del animal (ej. "vacunado", "adoptado").
4. `PRIMARY KEY (id)`: El campo `id` es clave primaria (único y no nulo).

---

## 🎯 Conclusión

* Se define una base de datos y una tabla estructurada.
* Se prepara el entorno para insertar y consultar datos de forma organizada.
