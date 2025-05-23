# Valores _Truthy_ y _Falsy_ en JavaScript

En JavaScript, los valores pueden evaluarse en **contextos booleanos** (como en estructuras condicionales).  
Cuando esto ocurre, el motor realiza una **coerción a booleano**, y los valores son clasificados como:

- **Truthy**: evaluados como `true`

- **Falsy**: evaluados como `false`

Esto es esencial para el control de flujo en condiciones (`if`, `while`, operadores lógicos, etc.).

Ver más sobre coerción: [[12 COERCION EN JAVASCRIPT]]

---

## ❌ Valores _Falsy_

Un valor _falsy_ es aquel que se evalúa como `false` en un contexto booleano.

|Valor|Resultado|
|---|---|
|`false`|`false`|
|`0`|`false`|
|`""` (string vacío)|`false`|
|`null`|`false`|
|`undefined`|`false`|
|`NaN`|`false`|

### Ejemplos falsy

```javascript
Boolean(0);           // false
Boolean("");          // false
Boolean(null);        // false
Boolean(undefined);   // false
Boolean(NaN);         // false
Boolean(false);       // false
```

### Coerción implícita (no recomendada)

```javascript
!!0;           // false
!!"";          // false
!!undefined;   // false
```

---

## ✅ Valores _Truthy_

Un valor _truthy_ es aquel que **no es falsy**, por lo tanto, se evalúa como `true`.

|Ejemplo|Resultado|
|---|---|
|`12`|`true`|
|`"hola"`|`true`|
|`true`|`true`|
|`[1, 2, 3]`|`true`|
|`function() {}`|`true`|
|`{ a: 1 }`|`true`|
|`[]` (array vacío)|`true`|
|`{}` (objeto vacío)|`true`|

### Ejemplos truthy

```javascript
Boolean(12);             // true
Boolean("hola");         // true
Boolean(true);           // true
Boolean([1, 2, 3]);      // true
Boolean(function() {});  // true
Boolean({ a: 1 });       // true
Boolean([]);             // true
Boolean({});             // true
```

> ℹ️ Incluso un **array vacío** (`[]`) o un **objeto vacío** (`{}`) se consideran _truthy_.

---

## Conclusión

- **Falsy**: valores que resultan `false` al convertirlos a booleano.

- **Truthy**: cualquier valor que no sea falsy.

Estos conceptos son clave para escribir condicionales limpias y seguras en JavaScript.
