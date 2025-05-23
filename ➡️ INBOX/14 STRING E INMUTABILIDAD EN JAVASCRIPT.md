# Strings e Inmutabilidad en JavaScript

## 🔍 ¿Qué significa que los strings son inmutables?

En JavaScript, los **strings son inmutables**, lo que quiere decir que **no se pueden modificar una vez creados**. 

[[10 TIPOS DE DATOS]]

Aunque puedes **reasignar una nueva cadena a la variable**, no puedes cambiar directamente los caracteres individuales de la cadena existente.

---

## ✏️ Ejemplo práctico

```javascript
// Asignamos una string a la variable miSaludo
let miSaludo = "¡Jola, mundo!";
console.log(miSaludo); // Output: ¡Jola, mundo!

// Intentamos modificar el segundo carácter (índice 1)
miSaludo[1] = "H";
console.log(miSaludo); // Output: ¡Jola, mundo! (no cambia)

// Reasignamos un nuevo valor completamente
miSaludo = "¡Hola, mundo!";
console.log(miSaludo); // Output: ¡Hola, mundo!
```

---

## 🧠 ¿Qué aprendimos?

- ❌ No se pueden modificar directamente los caracteres de un string.
    
- ✅ Sí se puede **reasignar** un nuevo string a la variable.
    

Esto es un reflejo de la **inmutabilidad de los strings** en JavaScript:

> _"No puedes cambiar una cadena directamente, pero puedes reemplazarla completamente."_
