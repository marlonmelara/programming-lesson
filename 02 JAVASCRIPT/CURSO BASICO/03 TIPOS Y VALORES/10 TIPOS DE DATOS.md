# Tipos de Datos en JavaScript

En JavaScript, **todos los valores** pertenecen a uno de dos grandes grupos:

- **Tipos primitivos**

- **Tipos de objeto**

Los **valores primitivos** son inmutables y se **pasan por valor**.  
Los **objetos** son estructuras más complejas y se **pasan por referencia**.

---

## 🔹 Tipos Primitivos

Los tipos primitivos representan **datos simples e indivisibles**.

|Tipo|Descripción|
|---|---|
|`String`|Texto entre comillas simples `'Hola'` o dobles `"Mundo"`.|
|`Number`|Números enteros o decimales. Ej: `42`, `3.14`.|
|`Boolean`|Representa verdadero o falso: `true` o `false`.|
|`null`|Valor asignado intencionadamente para indicar "sin valor".|
|`undefined`|Valor de una variable **no inicializada**.|
|`Symbol`|Valor **único e inmutable**, útil como identificadores.|
|`BigInt`|Representa enteros muy grandes. Ej: `1234567890123456789012345678901234567890n`|

### Ejemplos tipos primitivos

```javascript
let mensaje = "Hola Mundo";      // String
let edad = 30;                   // Number
let activo = true;               // Boolean
let usuario = null;             // Null
let respuesta;                  // Undefined
let id = Symbol("id");          // Symbol
let numeroGrande = 12345678901234567890n; // BigInt
```

---

## 🔸 Tipos de Objeto

Los objetos permiten almacenar **colecciones de datos y funcionalidades**.

|Tipo|Descripción|
|---|---|
|`Object`|Colección de pares clave-valor. Ej: `{ nombre: "Ana" }`|
|`Array`|Lista ordenada de valores. Ej: `[1, 2, 3]`|
|`Function`|Bloque reutilizable de código que puede ser invocado.|

### Ejemplos tipo objetos

```javascript
let persona = { nombre: "Juan", edad: 25 };   // Object
let numeros = [1, 2, 3, 4];                   // Array
function saludar() { console.log("Hola"); }  // Function
```

---

## 📌 JavaScript es Dinámicamente Tipado

JavaScript no requiere declarar el tipo de variable:  
el **tipo se infiere automáticamente** en tiempo de ejecución.

```javascript
let x = "texto"; // ahora x es String
x = 100;         // ahora x es Number
```

---

## Conclusión

- Usa **tipos primitivos** para representar valores simples.

- Usa **objetos** para estructuras complejas o funcionalidades.

- Recuerda que JavaScript puede cambiar dinámicamente el tipo de las variables.
