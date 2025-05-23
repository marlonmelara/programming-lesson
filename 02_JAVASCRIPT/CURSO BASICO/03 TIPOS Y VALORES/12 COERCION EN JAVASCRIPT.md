# Coerción en JavaScript

La **coerción** es el proceso mediante el cual se **transforma el tipo de dato de una variable** a otro.

JavaScript, al ser un lenguaje **débil y dinámicamente tipado**, permite este cambio de tipo de forma **implícita o explícita**.
[[06 TIPADO DEBIL VS TIPADO INFERIDO]]

---

## 🔹 Coerción Implícita

La **coerción implícita** ocurre cuando **JavaScript convierte automáticamente los tipos de datos** durante la ejecución del programa, especialmente cuando se combinan diferentes tipos en una operación.

> ⚠️ Esta transformación puede generar resultados inesperados si no se controla correctamente.

### Ejemplos coerción implícita

```javascript
4 + "7"     // "47"  → concatena número y string
4 * "7"     // 28    → convierte string a número
2 + true    // 3     → true se convierte en 1
false - 3   // -3    → false se convierte en 0
!3          // false → 3 es truthy, negado es false
```

🧠 **Recomendación**: Si quieres tener control del tipo de datos, **evita depender de la coerción implícita.**

---

## 🔸 Coerción Explícita

La **coerción explícita** se realiza de forma **intencional** por el programador, utilizando funciones como:

- `Number()` → convierte a número

- `String()` → convierte a cadena de texto

- `Boolean()` → convierte a valor lógico

### Ejemplos coerción explícita

```javascript
Number("47");   // 47
String(51);     // "51"
Boolean(1);     // true
```

### Verificación con `typeof`

```javascript
typeof Number("47");   // 'number'
typeof String(51);     // 'string'
typeof Boolean(1);     // 'boolean'
```

---

## 🧩 Conclusión

|Tipo de Coerción|¿Quién la realiza?|Control del resultado|¿Es recomendable?|
|---|---|---|---|
|Implícita|JavaScript|❌ No|⚠️ Solo si se entiende bien|
|Explícita|El programador|✅ Sí||
