# ¿Qué es el Tipado Inferido en JavaScript?

## ¿Qué es el Tipado Inferido?

El **tipado inferido** es la capacidad de un lenguaje para **deducir automáticamente el tipo de dato de una variable** a partir del valor que se le asigna, sin que el programador lo indique explícitamente.

### Ejemplo en JavaScript

``` javascript
let x = 123; // Se infiere que x es un número.
```

En JavaScript, esta inferencia no es formal como en lenguajes con tipado estático, pero se puede observar como comportamiento natural del lenguaje.

---

## Tipado Débil vs Tipado Inferido

### Tipado Débil

- Permite **asignar un valor de un tipo a una variable de otro tipo**.

- JavaScript convierte automáticamente los tipos según sea necesario.

``` javascript
let x = 1; 
x = "hola"; // Válido, ahora x es una cadena.`
```

Este comportamiento hace que JavaScript sea **flexible pero propenso a errores** si no se maneja con cuidado.

### Tipado Inferido

- Se refiere a **deducir el tipo en el momento de asignación**.

- No se impide el cambio posterior de tipo debido al tipado débil.

---

## TypeScript: Inferencia y Tipado Estático

**TypeScript**, un superconjunto de JavaScript, expande estas capacidades mediante:

- **Comprobación de tipos en tiempo de compilación**.

- **Inferencia más rigurosa** y opción de tipado explícito.

### Ejemplo en TypeScript

```typescript
function add(a: number, b: number): number {   return a + b; }
```

Esto proporciona mayor seguridad y ayuda a detectar errores antes de ejecutar el código.

---

## Conclusión

|Característica|JavaScript|TypeScript|
|---|---|---|
|Tipado Inferido|✔️ Sí, pero informal|✔️ Sí, con comprobación estricta|
|Tipado Débil|✔️ Sí|❌ No, requiere tipos consistentes|
|Tipado Estático|❌ No|✔️ Sí|

JavaScript ofrece **flexibilidad y rapidez**, pero puede llevar a errores si no se gestionan los tipos con cuidado. TypeScript agrega **seguridad y claridad** al usar tipado estático e inferencia avanzada.
