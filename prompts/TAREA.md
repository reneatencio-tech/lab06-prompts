
# Tarea: Mi prompt profesional

**Curso:** Diseño de Interfaces de Programación Avanzado  
**Laboratorio:** N.º 06 – Ingeniería de Prompts  
**Proyecto:** TiendaTec – Sistema de gestión de productos  
**Tecnología:** Java, Java Swing y Programación Orientada a Objetos (POO)

---

## Funcionalidad elegida

Para esta actividad elegí desarrollar **TiendaTec**, una aplicación para gestionar los productos de una tienda pequeña utilizando Java.

La funcionalidad principal consiste en registrar productos con su código, nombre, precio y stock, así como consultar, actualizar y eliminar sus datos. Además, el programa debe calcular el valor total del inventario.

Mi objetivo fue comprobar cómo mejora la respuesta de una inteligencia artificial cuando se utilizan instrucciones progresivamente más específicas, pasando de un prompt básico a uno profesional.

---

## Versión 1: prompt básico

### Prompt utilizado

> Crea un programa en Java para gestionar productos de una tienda.

### Resultado obtenido

La inteligencia artificial generó un programa en Java utilizando programación orientada a objetos y una interfaz de consola.

El programa incluía las siguientes funcionalidades:

- Registrar nuevos productos.
- Mostrar los productos registrados.
- Buscar productos mediante su código.
- Actualizar precios y stock.
- Eliminar productos.
- Calcular el valor total del inventario.

### Análisis de la versión 1

El resultado permitió identificar las funcionalidades básicas del sistema. Sin embargo, al tratarse de una instrucción general, la inteligencia artificial decidió por sí misma la estructura y la forma de interacción.

No se especificó que debía utilizarse Java Swing, ni se establecieron criterios detallados de validación o presentación.

**Conclusión:** El prompt básico generó una solución inicial útil, pero con poco control sobre las características del programa.

---

## Versión 2

### Prompt utilizado

> Actúa como un desarrollador de software especializado en Java y programación orientada a objetos.
>
> Estoy desarrollando una aplicación llamada TiendaTec para gestionar los productos de una tienda pequeña.
>
> Crea un programa en Java utilizando Swing que permita registrar productos con código, nombre, precio y stock; mostrar los productos en una tabla, buscar productos por código, actualizar sus datos, eliminar productos y calcular el valor total del inventario.
>
> Organiza el programa utilizando una clase Producto con atributos privados, una clase Inventario para administrar los productos y una clase TiendaTec para la interfaz gráfica.
>
> Explica brevemente la responsabilidad de cada clase y presenta el código Java correspondiente.

### Resultado obtenido

En esta segunda versión, la inteligencia artificial presentó una solución más cercana a las necesidades del proyecto.

El sistema incorporó:

- Una interfaz gráfica desarrollada con Java Swing.
- Tres clases: `Producto`, `Inventario` y `TiendaTec`.
- Una tabla `JTable` para visualizar productos.
- Una colección `ArrayList` para almacenar los registros.
- Operaciones de registro, búsqueda, actualización y eliminación.
- Cálculo del valor total del inventario.

### Análisis de la versión 2

Al incorporar un rol profesional, contexto y requisitos específicos, la respuesta fue más organizada.

La inteligencia artificial comprendió que necesitaba una aplicación de escritorio y no solamente un programa de consola.

Sin embargo, identifiqué que todavía era necesario precisar aspectos relacionados con la validación de datos, la distribución de los componentes gráficos y las pruebas de funcionamiento.

**Conclusión:** El segundo prompt mejoró considerablemente la solución porque estableció requisitos funcionales y una estructura de clases.

---

## Versión 3: prompt final

### Prompt utilizado

> Actúa como un desarrollador senior de Java especializado en programación orientada a objetos y aplicaciones de escritorio con Swing.
>
> **Contexto:** Estoy desarrollando TiendaTec, una aplicación académica para gestionar los productos de una tienda pequeña.
>
> **Objetivo:** Crear una aplicación Java Swing que permita registrar, listar, buscar, actualizar y eliminar productos, además de calcular el valor total del inventario.
>
> **Requisitos:**
>
> 1. Utilizar tres clases: Producto, Inventario y TiendaTec.
> 2. Cada producto tendrá código, nombre, precio y stock.
> 3. Aplicar encapsulamiento con atributos privados.
> 4. Utilizar ArrayList para almacenar los productos temporalmente.
> 5. Mostrar los productos mediante JTable.
> 6. Validar campos vacíos, códigos duplicados, precios negativos y stock negativo.
> 7. Confirmar antes de eliminar un producto.
> 8. Actualizar automáticamente la tabla y el valor total después de cada operación.
> 9. Utilizar correctamente BorderLayout y JPanel para evitar que los componentes se superpongan.
> 10. Mantener el código sencillo, comprensible y compatible con VS Code.
>
> **Restricciones:**
>
> - No utilizar bases de datos.
> - No utilizar bibliotecas externas.
> - No utilizar conceptos innecesariamente avanzados.
> - Entregar código completo, sin omitir métodos.
>
> **Formato de respuesta:** Explica la estructura y responsabilidad de las clases, presenta el código Java completo de cada archivo, incluye instrucciones para ejecutarlo en VS Code y propone cinco casos de prueba con sus resultados esperados.

### Resultado obtenido

La inteligencia artificial presentó una propuesta más completa, organizada y detallada.

La respuesta incluyó:

- Explicación de la arquitectura del proyecto.
- Código Java de las tres clases.
- Uso de `JFrame`, `JPanel`, `JTable` y `BorderLayout`.
- Validaciones de campos obligatorios y valores numéricos.
- Prevención de códigos duplicados.
- Confirmación antes de eliminar registros.
- Actualización automática de la tabla y del inventario.
- Instrucciones de compilación y ejecución en VS Code.
- Cinco casos de prueba con resultados esperados.

### Análisis de la versión 3

El prompt final permitió establecer claramente qué debía desarrollar la inteligencia artificial, cómo debía organizar el código y qué condiciones debía cumplir.

También incorporó restricciones para evitar soluciones innecesariamente complejas.

La respuesta presentó una estructura más adecuada para un proyecto académico y permitió identificar con mayor facilidad los archivos, métodos y procedimientos necesarios.

**Conclusión:** La tercera versión produjo la propuesta más completa de las tres. Sin embargo, su funcionamiento debe comprobarse mediante compilación y pruebas reales.

---

## Componentes del prompt final

| Componente | Descripción | Aplicación en TiendaTec |
|---|---|---|
| Rol | Define el perfil que debe asumir la IA. | Desarrollador senior especializado en Java Swing. |
| Contexto | Explica la situación y el proyecto. | Aplicación académica TiendaTec para una tienda pequeña. |
| Objetivo | Establece el resultado esperado. | Crear un sistema de gestión de productos. |
| Instrucciones | Detalla las funcionalidades y características. | Registrar, listar, buscar, actualizar y eliminar productos. |
| Restricciones | Establece límites para la solución. | Sin bases de datos ni bibliotecas externas. |
| Formato | Indica cómo debe presentarse la respuesta. | Explicación, código Java, ejecución y casos de prueba. |
| Criterios de calidad | Define las condiciones que debe cumplir el resultado. | Validaciones, encapsulamiento y organización de la interfaz. |

---

## Evaluación del resultado

Para evaluar los resultados, comparé las tres versiones considerando la claridad de las instrucciones, la organización del código y las funcionalidades propuestas.

| Criterio | Versión 1 | Versión 2 | Versión 3 |
|---|---|---|---|
| Claridad del prompt | Básica | Buena | Muy detallada |
| Contexto del proyecto | Limitado | Definido | Completo |
| Interfaz Java Swing | No | Sí | Sí |
| Organización en tres clases | No | Sí | Sí |
| Operaciones CRUD | Sí | Sí | Sí |
| Validaciones | Básicas | Parciales | Más completas |
| Distribución gráfica | No aplica | Requiere mejoras | Mejor organizada |
| Casos de prueba propuestos | No | No | Sí |
| Instrucciones de ejecución | Limitadas | Básicas | Detalladas |

### Reflexión personal

Durante esta actividad comprobé que no basta con solicitar a una inteligencia artificial que cree un programa. Es necesario explicar el contexto, definir las funcionalidades, establecer restricciones e indicar cómo debe presentarse el resultado.

La primera versión me permitió obtener una solución inicial. La segunda mejoró la estructura del programa y la tercera incorporó requisitos de calidad y criterios de validación.

Considero que el prompt final fue el más efectivo porque redujo las ambigüedades y orientó la respuesta hacia las necesidades específicas de mi proyecto.

También comprendí que una respuesta detallada no garantiza que el programa funcione correctamente. Por ello, es importante revisar, compilar y probar el código generado.

---

## Errores que evité

Durante la elaboración y mejora de los prompts procuré evitar los siguientes errores:

1. **Instrucciones demasiado generales:** Reemplacé una solicitud básica por indicaciones específicas sobre el funcionamiento del sistema.
2. **Falta de contexto:** Expliqué que estaba desarrollando TiendaTec como proyecto académico.
3. **No definir la tecnología:** Especifiqué el uso de Java Swing para desarrollar una aplicación de escritorio.
4. **No establecer la estructura:** Definí las clases Producto, Inventario y TiendaTec.
5. **Omitir validaciones:** Solicité controles para campos vacíos, códigos duplicados y valores negativos.
6. **No considerar el diseño gráfico:** Indiqué que debían utilizarse paneles y administradores de distribución para evitar componentes superpuestos.
7. **No establecer restricciones:** Señalé que no debían utilizarse bases de datos ni bibliotecas externas.
8. **No solicitar pruebas:** Incorporé cinco casos de prueba con resultados esperados.
9. **No definir el formato de respuesta:** Solicité explicaciones, código completo e instrucciones para ejecutar el proyecto.

### Conclusión final

El desarrollo de esta tarea me permitió comprender la importancia de la ingeniería de prompts en la programación.

Aprendí que una instrucción bien estructurada permite obtener respuestas más precisas, organizadas y adaptadas a las necesidades del usuario.

La evolución de las tres versiones de TiendaTec demuestra que incorporar rol, contexto, objetivo, instrucciones, restricciones y formato contribuye a mejorar la calidad de las soluciones generadas por inteligencia artificial.

Finalmente, comprendí que la inteligencia artificial es una herramienta de apoyo al desarrollo de software, pero la revisión y validación del resultado siguen siendo responsabilidad del programador.
