# Bitácora de prompts

Laboratorio N.° 06: Fundamentos de Ingeniería de Prompts.

**Curso:** Diseño de Interfaces de Programación Avanzado

**Herramienta de IA utilizada:** ChatGPT

## Ejercicio 2: Tokens y ventana de contexto

### Experimento 1: Conteo de tokens

Se analizaron tres textos utilizando el tokenizador
de OpenAI, con la opción GPT-5.x & O1/3, para comparar
la cantidad de caracteres y tokens.

| Texto | Caracteres | Tokens |
|-------|-----------:|-------:|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 30 | 7 |
| desafortunadamente | 18 | 4 |

**Análisis de resultados:**

Durante el experimento comprobé que la cantidad de
tokens no coincide necesariamente con la cantidad
de palabras ni de caracteres.

La oración en español presentó 34 caracteres y
7 tokens, mientras que la oración en inglés
presentó 30 caracteres y también 7 tokens.

Asimismo, observé que la palabra
"desafortunadamente", a pesar de ser una sola
palabra, se dividió en 4 tokens.

**Conclusión:**

Comprendí que los modelos de lenguaje procesan
el texto mediante unidades denominadas tokens,
las cuales pueden representar palabras completas,
fragmentos de palabras o signos de puntuación.

Este conocimiento es importante para comprender
el procesamiento de información y los límites
de contexto de los modelos de inteligencia artificial.

### Experimento 2: Conversación nueva

Se abrió una nueva conversación utilizando el modo
incógnito del navegador, sin proporcionar el
prompt inicial.

**Respuesta obtenida:**

No tengo información suficiente en esta conversación
para identificar el nombre de tu aplicación ni la
tecnología con la que está desarrollada.

**Resultado:** La IA no pudo identificar los datos
porque no tenía disponible el contexto anterior.

#### Análisis comparativo

Durante el experimento comprobé que el contexto
de una conversación influye directamente en las
respuestas de un modelo de inteligencia artificial.

En la primera prueba, ChatGPT identificó
correctamente el nombre TiendaTec y la tecnología
Java Swing porque ambos datos se habían
proporcionado previamente.

En la segunda prueba, al utilizar una conversación
nueva en modo incógnito, el modelo indicó que
no contaba con información suficiente para responder.

#### Conclusión

Comprendí que los modelos de lenguaje utilizan
la información disponible en el contexto de una
conversación para generar respuestas coherentes.

Asimismo, aprendí que es importante proporcionar
instrucciones claras y antecedentes suficientes
cuando se inicia una nueva conversación.

El experimento también permitió diferenciar
el contexto de una conversación de las funciones
de memoria que pueden existir entre conversaciones.

## Ejercicio 3: Temperatura

Se implementó el programa SimuladorTemperatura.java,
que utiliza seis posibles nombres para una
aplicación de biblioteca.

El programa calcula las probabilidades mediante
la función Softmax y realiza cinco selecciones
aleatorias por cada ejecución.

## 3. Pruebas realizadas

| Temperatura | BiblioTec | Comportamiento |
|-------------|-----------|----------------|
| 0.0 | 100.0 % | Determinista |
| 0.5 | 65.3 % | Conservador |
| 1.0 | 44.5 % | Moderado |
| 1.8 | 32.2 % | Mayor diversidad |

## 4. Comandos utilizados

```bash
javac SimuladorTemperatura.java
java SimuladorTemperatura 0
java SimuladorTemperatura 0.5
java SimuladorTemperatura 1
java SimuladorTemperatura 1.8
```

## 5. Análisis de resultados

Con temperatura 0, el programa seleccionó
siempre BiblioTec.

Con temperatura 0.5, BiblioTec mantuvo
una probabilidad elevada del 65.3 %.

Con temperatura 1.0, la distribución fue
más equilibrada.

Con temperatura 1.8, aumentaron las
probabilidades de las opciones menos frecuentes.

## 6. Conclusiones

Se comprobó que una temperatura baja favorece
las respuestas con mayor puntuación.

Una temperatura alta genera mayor diversidad
en las respuestas seleccionadas.

El laboratorio permitió comprender el
funcionamiento básico del parámetro temperatura
mediante una simulación práctica en Java.

## Ejercicio 4: Prompt vago vs. estructurado


### 4.1. Objetivo
Comparar la calidad de las respuestas generadas por
una inteligencia artificial utilizando un prompt
vago y otro estructurado.

### 4.2. Prompt vago

```text
Hazme una descripcion de un sistema de biblioteca.
```

**Resultado:** La IA generó una descripción general
de cuatro párrafos, incluyendo el objetivo, los
usuarios y diversas funcionalidades, pero sin una
estructura específica.

### 4.3. Prompt estructurado

```text
Actua como analista de sistemas. Redacta una
descripcion breve de un sistema web para gestionar
prestamos de libros en una biblioteca.
Incluye objetivo, usuarios principales y 3
funcionalidades clave. Utiliza un lenguaje claro
y profesional y presenta el resultado en 3 parrafos.
```

**Resultado:** La IA presentó una descripción
profesional de tres párrafos: objetivo, usuarios
principales y tres funcionalidades clave.

### 4.4. Comparación

| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona el objetivo del sistema | Sí | Sí |
| Menciona a los usuarios principales | Sí | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Está en 3 párrafos | No | Sí |
| Lo usaría en un informe real | No | Sí |

### 4.5. Análisis

El prompt vago permitió obtener información
general, pero no estableció criterios específicos
de extensión, estructura ni contenido.

El prompt estructurado proporcionó instrucciones
claras sobre el rol, objetivo, contenido y formato,
generando una respuesta más organizada y útil.

### 4.6. Conclusión

Se comprobó que la calidad de un prompt influye
en la precisión y organización de las respuestas
de una inteligencia artificial.

Un prompt estructurado reduce la ambigüedad
y permite obtener resultados más adecuados
para una necesidad específica.

## Ejercicio 5: Anatomía de un prompt

### Nivel 1: Prompt básico

**Prompt utilizado:**

```text
Crea un programa en Java.
```

**Resultado obtenido:**

ChatGPT no generó directamente un programa. En su lugar, solicitó que especificara qué tipo de aplicación deseaba desarrollar y presentó ejemplos como calculadora, inventario, sistema bancario y sistema de ventas.

**Observación:**

Comprobé que una instrucción demasiado general no garantiza una respuesta concreta. Al no definir el objetivo ni las funcionalidades del programa, la IA necesitó solicitar información adicional antes de generar el código. Esto demuestra la importancia de formular prompts claros y específicos.

### Nivel 2: Prompt con rol

**Prompt utilizado:**

```text
Actua como desarrollador Java. Crea un programa en Java.
```

**Resultado obtenido:**

ChatGPT asumió el rol de desarrollador Java y mencionó que utilizaría buenas prácticas de programación, código limpio y programación orientada a objetos. Sin embargo, solicitó información adicional sobre el programa y presentó alternativas como Java básico, Java Swing, JavaFX y bases de datos.

**Observación:**

Al incorporar el rol de desarrollador Java, observé una respuesta más técnica y especializada que en el primer nivel. No obstante, la IA todavía necesitó aclaraciones porque no había definido la finalidad del programa. Comprendí que asignar un rol mejora la orientación de la respuesta, pero también es necesario proporcionar un contexto específico.

### Nivel 3: Prompt con rol y contexto

**Prompt utilizado:**

```text
Actua como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.
```

**Resultado obtenido:**

ChatGPT generó directamente una propuesta de sistema de gestión de productos para una tienda, utilizando programación orientada a objetos en Java.

El proyecto fue organizado en tres clases: `Producto.java`, `Inventario.java` y `Main.java`.

La aplicación propuesta permite registrar, listar, buscar, actualizar y eliminar productos, además de calcular el valor total del inventario. También incluye validaciones de datos, un ejemplo de ejecución y explicaciones sobre los conceptos de Java utilizados.

**Observación:**

Al agregar el contexto de gestionar los productos de una tienda, observé una mejora importante en la respuesta. A diferencia de los niveles anteriores, ChatGPT ya no solicitó aclaraciones y generó código relacionado directamente con el objetivo.

Sin embargo, la aplicación fue planteada para ejecutarse en consola, debido a que no especifiqué el tipo de interfaz gráfica que necesitaba.

**Conclusión:**

Comprendí que proporcionar un contexto específico permite obtener respuestas más completas y útiles. También identifiqué que, para controlar mejor el resultado, es necesario indicar requisitos técnicos como la tecnología, las funcionalidades y el formato de entrega.

### Nivel 4: Prompt estructurado

**Prompt utilizado:**

Se utilizó un prompt estructurado en el que se definieron el rol de desarrollador Java, el contexto del proyecto TiendaTec, el objetivo de crear una aplicación de escritorio, siete requisitos funcionales, restricciones técnicas y el formato esperado de la respuesta.

**Resultado obtenido:**

ChatGPT generó una propuesta de aplicación denominada TiendaTec, desarrollada en Java Swing y organizada en tres clases: `Producto.java`, `Inventario.java` y `TiendaTec.java`.

La solución incluye una interfaz gráfica con campos para ingresar información, una tabla para visualizar productos y botones para registrar, buscar, actualizar, eliminar y calcular el valor total del inventario.

También presentó validaciones de datos, explicaciones de las clases, instrucciones para ejecutar el programa en Visual Studio Code y ejemplos de funcionamiento.

**Observación:**

Observé que este nivel permitió obtener una respuesta más precisa y organizada. A diferencia del Nivel 3, donde ChatGPT propuso una aplicación de consola, en el Nivel 4 generó código para una interfaz gráfica utilizando Java Swing, tal como se había solicitado.

Además, al establecer restricciones y un formato de respuesta, el contenido fue más específico y adecuado para el proyecto.

**Conclusión:**

Comprendí que un prompt estructurado mejora considerablemente la calidad y pertinencia de las respuestas de la inteligencia artificial. Definir el rol, contexto, objetivo, requisitos, restricciones y formato permite orientar mejor la generación del código y reducir las interpretaciones incorrectas.

Sin embargo, también aprendí que el código generado debe compilarse y probarse antes de considerarlo completamente funcional.

### Nivel 5: Prompt con formato

**Prompt utilizado:**

Actúa como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda, usando una clase Producto con los atributos código, nombre, precio y stock.

Explica primero la estructura de la clase y luego presenta el código Java.

**Resultado obtenido:**

ChatGPT generó una respuesta organizada en cuatro secciones. Primero explicó la estructura de la clase `Producto`, identificando sus atributos, tipos de datos y métodos. Posteriormente presentó el código fuente de dos archivos: `Producto.java` y `Principal.java`.

El programa propuesto permite crear productos, consultar sus datos, modificar precios y cantidades, actualizar el stock y calcular el valor del inventario.

También incluyó un ejemplo de ejecución y una conclusión sobre los conceptos de programación orientada a objetos utilizados.

**Análisis:**

Observé que, al agregar una instrucción sobre el formato de la respuesta, ChatGPT organizó mejor la información. A diferencia de los niveles anteriores, en esta oportunidad presentó primero la explicación teórica y después el código, facilitando la comprensión del funcionamiento del programa.

**Conclusión:**

Comprendí que definir el formato esperado dentro de un prompt permite obtener respuestas más ordenadas y fáciles de interpretar. Esta técnica resulta útil para aprender programación porque permite comprender primero los conceptos y posteriormente analizar su aplicación en el código Java.

La respuesta cumplió con el formato solicitado, aunque el código todavía requiere pruebas de compilación y ejecución para confirmar su funcionamiento.