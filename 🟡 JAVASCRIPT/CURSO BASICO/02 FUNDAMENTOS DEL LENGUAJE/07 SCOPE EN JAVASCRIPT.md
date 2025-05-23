# ¿Qué es el _Scope_ en JavaScript?

El **scope** (alcance) define el **entorno en el que una variable puede ser accedida** dentro del código. En otras palabras, determina **dónde está disponible una variable** dependiendo de dónde se haya declarado.

## 🔍 Ejemplo conceptual

> Imagina que perdiste tus llaves. Las buscas primero en los lugares más cercanos y luego te alejas. En este ejemplo:
>
> - **Tú** eres el motor de JavaScript.
>
> - **Las llaves** son las variables.
>
> - **El entorno donde buscas** es el scope.
>

---

## Tipos de _Scope_

### 1. **Scope Global**

- Variables declaradas **fuera de funciones o bloques**.

- Son **accesibles desde cualquier parte** del código.

``` javascript
var nombre = "JavaScript";

function saludar() {
  console.log("Hola " + nombre); // Hola JavaScript
}

saludar(); // Accede correctamente a la variable global
```

### 2. **Scope Local**

- Variables declaradas **dentro de funciones o bloques** `{}`.

- Solo están disponibles dentro de ese **bloque específico**.

```javascript
function saludo() {
  let nombre = "Andres";
  console.log(nombre); // "Andres"
}

saludo();
console.log(nombre); // ❌ ReferenceError: nombre is not defined
```

> ⚠️ JavaScript **no busca en scopes más internos** si no encuentra una variable. Solo va **del scope local al global**, nunca al revés.

---

## Scope Chaining (_Cadena de Scope_)

Cuando haces referencia a una variable, **JavaScript la busca en el entorno más cercano**. Si no la encuentra, continúa buscando hacia afuera.

> 👉 **No busca hacia adentro** de funciones que ya han terminado su ejecución.

---

## Ejemplo de análisis de _Scope_

```javascript
var miNombre = "Marlon"; // Global

function nombre() {
  var miApellido = "Melara"; // Local
  console.log(miNombre + " " + miApellido);
}

nombre();

console.log(miNombre);   // ✔️ "Marlon"
console.log(miApellido); // ❌ ReferenceError
```

### Explicación

- `miNombre` es global → accesible en cualquier parte.

- `miApellido` es local → **solo existe dentro de la función** `nombre()`.

- Acceder a `miApellido` fuera de esa función genera un error.

---

## Bloques como Scope

Cualquier bloque encerrado entre `{}` puede tener su propio scope:

```javascript
if (true) {
  let mensaje = "Hola";
}
console.log(mensaje); // ❌ ReferenceError
```
