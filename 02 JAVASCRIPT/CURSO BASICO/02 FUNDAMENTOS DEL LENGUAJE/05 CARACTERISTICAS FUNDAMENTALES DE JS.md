# Características Fundamentales de JavaScript

JavaScript es un lenguaje de programación versátil y ampliamente utilizado. [[01 QUE ES JAVASCRIPT]] Estas son algunas de sus características más destacadas:

## 1. Lenguaje Interpretado (¿o compilado?)

JavaScript es comúnmente conocido como un **lenguaje interpretado**, ya que:

- El código es ejecutado **línea por línea** por el motor del navegador (como **V8** en Chrome).

- No requiere un proceso de compilación previo.

- Permite una **respuesta inmediata** a los cambios durante el desarrollo.

Sin embargo, gracias a tecnologías como la **compilación JIT (Just-In-Time)**, también se comporta como un lenguaje **compilado en espíritu**:

- El motor transforma el código JS en un **formato intermedio binario** antes de su ejecución.

- Aplica **optimización** dinámica para mejorar el rendimiento.

- Esto permite detectar ciertos errores **antes de la ejecución** y ejecutar el código más eficientemente.

📌 En resumen:

> **JavaScript combina lo mejor de ambos mundos**: ejecución inmediata como un lenguaje interpretado y optimización de rendimiento como un lenguaje compilado.

🔗 Más sobre esto: [What’s in an Interpretation?](https://github.com/marlonmelara/You-Dont-Know-JS/blob/2nd-ed/get-started/ch1.md#whats-in-an-interpretation)

---

## 2. Orientado a Objetos

JavaScript permite trabajar con **objetos**, que combinan **datos (propiedades)** y **comportamientos (métodos)**.

Esto facilita:

- Representar entidades del mundo real (ej. un coche con propiedades como `color`, `modelo` y métodos como `acelerar()`).

- Organizar el código de forma **estructurada y reutilizable**.

🔗 Más detalles: Lenguaje orientado a objetos

---

## 3. Débilmente Tipado

JavaScript es un lenguaje **débilmente tipado** [[06 TIPADO DEBIL VS TIPADO INFERIDO]], lo que significa:

- Las variables pueden **cambiar de tipo de dato** durante la ejecución.

- El lenguaje realiza **conversiones automáticas** (a veces inesperadas).

Ejemplo:

```javascript
let variable = 5; 
variable = "ahora es un texto";
```

Esto permite flexibilidad, pero exige cuidado para evitar errores lógicos.

🔗 Más sobre esto: [Débilmente tipado](https://www.notion.so/Caracter-stica-D-bilmente-tipado-29270d6b4dfd4046baf41cdb216c11be?pvs=21)

---

## 4. Dinámico

JavaScript permite **modificar el código en tiempo de ejecución**, es decir:

- Puedes agregar o eliminar **objetos, funciones y variables** mientras el programa está corriendo.

- Esto lo hace ideal para aplicaciones web interactivas y **eventos en tiempo real**.

🔗 Ver más: [Naturaleza dinámica](https://www.notion.so/Caracter-stica-Din-mico-9f5f27ddd65c456e8703316c60db2955?pvs=21)

---

## Conclusión

JavaScript es:

- **Interpretado y compilado** (según el contexto).

- **Orientado a objetos**, ideal para estructurar código.

- **Débilmente tipado**, lo que permite flexibilidad pero requiere precaución.

- **Dinámico**, permitiendo gran adaptabilidad en tiempo real.

Estas características lo convierten en un lenguaje poderoso para el desarrollo moderno, especialmente en aplicaciones web.
