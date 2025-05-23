# Comprobar y convertir tipo de datos

## Comprobar el tipo de dato

Chequear el tipo de una variable en JavaScript es una tarea común para asegurar que los datos sean del tipo correcto. Esto se puede hacer usando la palabra clave `typeof`.

[[10 TIPOS DE DATOS]]

Esta devuelve una **cadena que indica el tipo** de la variable.

```javascript
let numero = 5;
console.log(typeof numero); // Devuelve "number"
```

---

## Conversión de tipos de datos

JavaScript es un **lenguaje dinámico**, lo que significa que los tipos de datos de una variable pueden cambiar durante la ejecución. Por lo tanto, a veces es necesario **convertir un tipo de dato a otro** para que el programa funcione correctamente.
[[06 TIPADO DEBIL VS TIPADO INFERIDO]]

### Ejemplo

Supongamos que tenemos una variable llamada `numero` con el valor `"5"`, que es una **cadena de texto**. Si necesitamos realizar operaciones matemáticas, debemos convertirla a un **número entero** usando `parseInt()`:

```javascript
let numero = "5";
let numeroEntero = parseInt(numero);
```

Ahora, `numeroEntero` contiene el valor `5`, que es un número entero.
