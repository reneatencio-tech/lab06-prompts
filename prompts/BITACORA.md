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

## Ejercicio 5: Anatomía de un prompt