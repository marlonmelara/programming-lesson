# ¿Qué puedo o no utilizar de ECMAScript?

## Compatibilidad con Navegadores

Cada navegador web **adopta las nuevas características de ECMAScript [[02 QUE ES ECMASCRIPT]] a su propio ritmo**. Esto significa que si usas una funcionalidad muy reciente, algunos navegadores podrían no reconocerla, provocando errores o fallos en tu aplicación.

### 🛠 Recomendación

Consulta el sitio [**Can I use?**](https://caniuse.com/) para verificar qué características de ECMAScript están **soportadas por cada navegador**. Esto es esencial para:

- Determinar qué puedes usar de forma segura.

- Adaptar tu código según el público objetivo y sus navegadores.

- Garantizar la funcionalidad del producto final.

---

## Compatibilidad: Hacia Atrás y Hacia Adelante

> **Resumen de You Don’t Know JS (YDKJSY)**

### Compatibilidad hacia atrás

JavaScript mantiene un fuerte compromiso con la **compatibilidad hacia versiones anteriores**. Esto significa que:

- El código válido escrito en 1995 **debería seguir funcionando hoy**.

- El comité **TC39** (encargado de la evolución de JavaScript) sigue el principio:

    > “¡No rompemos la web!”

Esta filosofía permite que JavaScript sea una **inversión estable a largo plazo**. Aunque mantener esta compatibilidad plantea desafíos, se considera esencial para la continuidad de proyectos existentes.

Cambios que podrían romper el funcionamiento del código antiguo son **raros y muy estudiados**, considerando cuidadosamente los pros y contras antes de implementarlos.

### Compatibilidad hacia adelante

A diferencia de HTML o CSS, JavaScript **no tiene compatibilidad hacia adelante**. Es decir:

- Si introduces una característica nueva y ejecutas el código en un motor de JS antiguo, **puede fallar completamente**.

- Los lenguajes declarativos (como HTML/CSS) simplemente **ignoran lo que no reconocen**. En JavaScript, esto **no es viable**, ya que puede conducir a errores impredecibles.

### En resumen

- ✅ **Compatibilidad hacia atrás**: Garantiza estabilidad y continuidad.

- ❌ **Sin compatibilidad hacia adelante**: Riesgo de errores en navegadores no actualizados.
