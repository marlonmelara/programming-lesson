# ¿Desde qué versión ECMAScript funciona el _Hoisting_ en JavaScript?

## 🔍 ¿Qué es el _Hoisting_?

**Hoisting** es el comportamiento por el cual las **declaraciones de variables y funciones se “mueven” al inicio del ámbito** (scope) en el que se encuentran, **durante la fase de compilación** del código.  

[[08 QUE ES EL HOISTING EN JAVASCRIPT]]  - [[07 SCOPE EN JAVASCRIPT]]

🔸 Este movimiento es interno: **el código no cambia visualmente**, pero el motor de JavaScript lo interpreta de esa forma.

---

## 📜 _Hoisting_ antes de ES6

Antes de **ECMAScript 2015 (ES6)**, JavaScript tenía un comportamiento clásico de hoisting con:

- Variables declaradas con `var`

- Funciones declaradas con `function`

### Ejemplo con `var`

```javascript
console.log(a); // undefined
var a = 5;
```

Internamente:

```javascript
var a;
console.log(a); // undefined
a = 5;
```

### Ejemplo con funciones

```javascript
saludo(); // "Hola"

function saludo() {
  console.log("Hola");
}
```

---

## 🆕 Cambios con ES6 (`let`, `const` y `=>`)

Con ES6, el hoisting **sigue ocurriendo**, pero con **diferencias importantes**:

### `let` y `const`

- También son elevadas, **pero no inicializadas**.

- Están en un estado llamado **“zona muerta temporal”** hasta que se alcanza su declaración.

```javascript
console.log(x); // ❌ ReferenceError
let x = 10;
```

### Funciones de flecha (`=>`)

- Al ser asignadas como expresiones a una variable (`const`, `let`, o `var`), **no se elevan como las funciones tradicionales**.

```javascript
saludo(); // ❌ ReferenceError

const saludo = () => {
  console.log("Hola");
};
```

---

## ✅ En resumen

|Declaración|¿Se eleva?|¿Se puede usar antes de declararse?|Comportamiento|
|---|---|---|---|
|`var`|✔️ Sí|✔️ Sí (como `undefined`)|Hoisting clásico|
|`let` / `const`|✔️ Sí|❌ No|Zona muerta temporal|
|`function`|✔️ Sí|✔️ Sí|Hoisting completo|
|`const nombre = () => {}`|✔️ Sí (la var)|❌ No|No se eleva la función|

---

## 📌 Conclusión

- El _hoisting_ ha estado presente **desde las primeras versiones de JavaScript**.

- **ES6 (2015)** introdujo cambios importantes en el comportamiento de hoisting:

  - `let` y `const` generan errores si se accede antes de la declaración.

  - Las funciones de flecha (`=>`) **no son elevadas** como las funciones tradicionales.

---
