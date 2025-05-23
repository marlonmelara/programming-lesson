# ¿Qué es el _Hoisting_ en JavaScript?

**Hoisting** (elevación) es el comportamiento por el cual las **declaraciones de variables y funciones** son movidas internamente **al inicio del scope más cercano** (_scope_ global o de función) **antes de ejecutar el código**.

[[07 SCOPE EN JAVASCRIPT]]

🔸 **Solo se elevan las declaraciones, no las asignaciones.**

---

## 🟦 Hoisting con `var`

Las variables declaradas con `var` son elevadas al inicio del _scope_, pero **se inicializan con `undefined`**.

### Ejemplo

```javascript
console.log(nombre); // undefined
var nombre = "Andres";
```

Internamente, JavaScript interpreta esto como:

```javascript
var nombre;
console.log(nombre); // undefined
nombre = "Andres";
```

---

## 🟨 Hoisting con `let` y `const`

Aunque `let` y `const` también son elevadas, **no son inicializadas automáticamente**, por lo que intentar acceder a ellas antes de su declaración genera un **ReferenceError**.

### Ejemplo variables

```javascript
console.log(nombre); // ❌ ReferenceError
let nombre = "Andres";
```

> ✅ Esto mejora la seguridad del código al evitar errores silenciosos como los que ocurren con `var`.

---

## 🟩 Hoisting en Funciones

Las **declaraciones de funciones** también se elevan, lo que permite llamarlas **antes de su definición**.

### Ejemplo funciones

```javascript
console.log(saludar()); // "Hola"

function saludar() {
  return "Hola";
}
```

Esto funciona porque las funciones se **almacenan completas en memoria** durante la fase de creación del contexto de ejecución.

---

## ✅ Buenas Prácticas

- Declara variables y funciones **al inicio de tu scope**.

- Prefiere `let` y `const` sobre `var` para evitar efectos secundarios de hoisting.

- Evita llamar funciones o variables **antes de declararlas**, aunque técnicamente sea posible con `var` o `function`.

---

## Recursos Recomendados

- 🔗 [MDN: Hoisting](https://developer.mozilla.org/es/docs/Glossary/Hoisting)

- ✍️ [¿Qué es el hoisting? – Medium](https://anamartinezaguilar.medium.com/qu%C3%A9-es-el-hoisting-327870f67b36)

- 📁 [Ejemplos prácticos - GitHub (jsBasico)](https://github.com/degranda/jsBasico-)

- [[09 HOISTING EN LAS VERSIONES DE ECMASCRIPT]]
