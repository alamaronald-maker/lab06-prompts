# Bitácora de Ingeniería de Prompts

**Laboratorio 06:** Fundamentos de Ingeniería de Prompts.

**Herramienta de IA usada:** ChatGPT.

## 1. Datos generales

- **Curso:** Diseño Avanzado de Interfaces de Programación
- **Laboratorio:** N.º 6 – Fundamentos de Ingeniería de Prompts
- **Estudiante:** José Ronald Alama Rodriguez
- **Fecha:** 10 de noviembre de 2026

## 2. Objetivo

Experimentar con diferentes técnicas de ingeniería de prompts para comprender cómo las instrucciones, el contexto y la estructura de una solicitud influyen en las respuestas generadas por un modelo de lenguaje.

## 3. Desarrollo de las actividades

### 3.1 Experimento 1: Influencia de las instrucciones

**Objetivo:** Comprobar cómo cambia la respuesta de un modelo de lenguaje cuando se modifica la claridad y el nivel de detalle de las instrucciones.

**Prompt básico:**

```text
Explícame el cambio climático.
```

**Prompt mejorado:**

```text
Actúa como un profesor de ciencias. Explícame qué es el cambio climático, cuáles son sus principales causas y consecuencias. Utiliza un lenguaje sencillo, incluye tres ejemplos de la vida cotidiana y termina con una conclusión.
```

**Resultado obtenido:**

La experimentación muestra que un prompt básico, como «Explícame el cambio climático», genera una solicitud general. En cambio, un prompt mejorado especifica el rol del modelo, el tema, los puntos que debe desarrollar, el lenguaje y la estructura de la respuesta.

Por ejemplo, al solicitar que actúe como profesor de ciencias, explique las causas y consecuencias, utilice lenguaje sencillo, incluya tres ejemplos cotidianos y termine con una conclusión, se obtiene una instrucción mucho más completa.

**Análisis:**

El prompt mejorado permite obtener una respuesta más clara, organizada y específica porque proporciona mayor contexto e indica exactamente qué información se necesita y cómo debe presentarse. Por ello, la calidad de las instrucciones influye directamente en la utilidad de la respuesta generada.

### 3.2 Ejercicio 2: Tokens y ventana de contexto

**Objetivo:** Identificar cómo el tokenizador divide diferentes textos en tokens y comprobar cómo funciona la ventana de contexto.

**Herramienta utilizada:** Tokenizador de OpenAI y ChatGPT.

**Actividad 1: Contar tokens**

Se analizaron tres textos utilizando el tokenizador de OpenAI.

**Resultados obtenidos:**

| Texto | Caracteres | Tokens |
|---|---:|---:|
| Los estudiantes programan en Java. | 34 | 7 |
| The students program in Java. | 29 | 6 |
| desafortunadamente | 18 | 4 |

**Análisis:**

Los resultados muestran que una misma idea puede utilizar diferente cantidad de tokens según el idioma. La oración en español obtuvo 7 tokens, mientras que su equivalente en inglés obtuvo 6 tokens.

Además, la palabra «desafortunadamente» se dividió en 4 tokens, aunque está formada por una sola palabra.

Esto demuestra que los tokens no equivalen necesariamente a palabras completas, ya que una palabra puede dividirse en varias partes.

**Actividad 2: Llenar la ventana de contexto**

En un chat nuevo de ChatGPT se envió el siguiente mensaje:

```text
Estoy desarrollando una aplicacion llamada TiendaTec en Java Swing para gestionar los productos de una tienda. Solo responde: Entendido.
```

**Actividad 3: Preguntar dentro del mismo chat**

Se realizó la siguiente pregunta en la misma conversación:

```text
¿Como se llama mi aplicacion y que tecnologia usa?
```

**Resultado obtenido en el mismo chat:**

ChatGPT respondió: «Tu aplicación se llama TiendaTec y utiliza Java Swing».

**Actividad 4: Preguntar en un chat nuevo**

Se abrió otra conversación y se envió exactamente la misma pregunta:

```text
¿Como se llama mi aplicacion y que tecnologia usa?
```

**Resultado obtenido en el chat nuevo:**

ChatGPT respondió que no tenía información suficiente en esa conversación para identificar el nombre de la aplicación ni la tecnología utilizada. También solicitó compartir el código fuente, una captura del proyecto o el archivo correspondiente para poder identificar esos datos.

**Análisis de la ventana de contexto:**

En la misma conversación, ChatGPT pudo identificar correctamente el nombre de la aplicación y la tecnología utilizada porque anteriormente se le había proporcionado esa información.

En cambio, en el chat nuevo no pudo identificar esos datos porque no se había proporcionado previamente el contexto de la aplicación.

Esta comparación demuestra que la ventana de contexto permite al modelo utilizar la información compartida anteriormente dentro de una conversación. Al iniciar un chat nuevo, esa información no está disponible automáticamente en el contexto de la conversación.

**Reflexión sobre los pasos 4 y 5:**

En el paso 4, ChatGPT recordó el nombre TiendaTec y la tecnología Java Swing porque ya le había proporcionado esos datos en la misma conversación.

En el paso 5, no pudo responder correctamente porque se inició un chat nuevo y no tenía la información anterior en su contexto.

### 3.3 Ejercicio 3: Temperatura

**Objetivo:** Observar cómo cambia la variabilidad de las respuestas al utilizar diferentes valores de temperatura.

**Herramienta utilizada:** ChatGPT, Java y simulador desarrollado en Java.

**Actividad 1: Observar la variabilidad del chat**

Se utilizó el siguiente prompt en tres chats nuevos:

```text
Propón 3 nombres para una aplicación de préstamo de libros de una biblioteca universitaria. Responde solo con la lista.
```

**Resultados obtenidos:**

- **Primer intento:** BiblioPréstamo, UniBook y BibliotecaApp.
- **Segundo intento:** BiblioPréstamo, UniLibro y BiblioConecta.
- **Tercer intento:** BiblioPréstamo, UniLibro y BookCampus.

**Análisis:**

Aunque se utilizó el mismo prompt, los nombres cambiaron entre los intentos. Esto demuestra que las respuestas de un modelo pueden presentar variabilidad incluso cuando las instrucciones son iguales.

**Actividad 2: Comprobar que Java está instalado**

Se ejecutó el siguiente comando en la terminal:

```powershell
java -version
```

**Resultado obtenido:**

Se comprobó que Java estaba instalado correctamente. La versión mostrada fue Java 25.0.5.

**Actividad 3: Crear y ejecutar el simulador**

Se creó la carpeta `simulador` y dentro de ella el archivo `SimuladorTemperatura.java`.

El programa permite representar cómo cambia la distribución de probabilidades cuando se utilizan diferentes valores de temperatura.

**Actividad 4: Compilar y ejecutar con distintas temperaturas**

Se compiló el programa con el comando:

```powershell
javac simulador/SimuladorTemperatura.java
```

Después se ejecutó con los valores de temperatura indicados en la práctica: 0.0, 0.5, 1.0 y 1.8.

**Resultados obtenidos:**

**Temperatura 0.0:**

```text
BiblioTec       100.0 %
LibroYa           0.0 %
PrestaLibro       0.0 %
LectoGo           0.0 %
PaginaLibre       0.0 %
NubeDeTinta       0.0 %

5 intentos: BiblioTec, BiblioTec, BiblioTec, BiblioTec, BiblioTec
```

**Temperatura 0.5:**

```text
BiblioTec        65.3 %
LibroYa          24.0 %
PrestaLibro       8.8 %
LectoGo           1.2 %
PaginaLibre       0.4 %
NubeDeTinta       0.2 %
```

**Temperatura 1.0:**

```text
BiblioTec        44.5 %
LibroYa          27.0 %
PrestaLibro      16.4 %
LectoGo           6.0 %
PaginaLibre       3.7 %
NubeDeTinta       2.4 %
```

**Temperatura 1.8:**

```text
BiblioTec        32.2 %
LibroYa          24.4 %
PrestaLibro      18.5 %
LectoGo          10.6 %
PaginaLibre       8.0 %
NubeDeTinta       6.4 %

Primera ejecución:
5 intentos: PrestaLibro, BiblioTec, PrestaLibro, BiblioTec, BiblioTec

Segunda ejecución:
5 intentos: LibroYa, PaginaLibre, BiblioTec, LibroYa, PaginaLibre
```

**Tabla comparativa de resultados:**

| Temperatura | BiblioTec | LibroYa | PrestaLibro | LectoGo | PaginaLibre | NubeDeTinta |
|---:|---:|---:|---:|---:|---:|---:|
| 0.0 | 100.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % | 0.0 % |
| 0.5 | 65.3 % | 24.0 % | 8.8 % | 1.2 % | 0.4 % | 0.2 % |
| 1.0 | 44.5 % | 27.0 % | 16.4 % | 6.0 % | 3.7 % | 2.4 % |
| 1.8 | 32.2 % | 24.4 % | 18.5 % | 10.6 % | 8.0 % | 6.4 % |

**Actividad 5: Ejecutar dos veces la misma temperatura**

Se ejecutó dos veces el simulador utilizando la temperatura 1.8.

Se observó que los porcentajes de probabilidad permanecieron iguales, pero los cinco nombres seleccionados cambiaron entre una ejecución y otra.

**Análisis:**

Con temperatura 0.0, el simulador seleccionó siempre la opción BiblioTec, que obtuvo el 100 % de probabilidad.

Con temperatura 0.5, BiblioTec continuó siendo la opción más probable, pero las demás alternativas comenzaron a tener mayor participación.

Con temperatura 1.0, las probabilidades se distribuyeron entre las seis opciones. Finalmente, con temperatura 1.8, la distribución fue más uniforme y aumentó la posibilidad de seleccionar nombres menos probables.

Al ejecutar dos veces la temperatura 1.8, los porcentajes permanecieron iguales, pero cambiaron los nombres seleccionados en los cinco intentos. Esto demuestra la variabilidad de la selección aleatoria.

**Reflexión sobre la temperatura:**

Al aumentar la temperatura, las probabilidades se distribuyen de manera más uniforme y aumenta la variedad de resultados. El simulador no inventa nombres nuevos porque solamente puede seleccionar las opciones que están definidas previamente en su código.

Por lo tanto, una temperatura baja favorece resultados más predecibles, mientras que una temperatura alta permite mayor variabilidad.

### 3.4 Ejercicio 4: Prompt vago vs estructurado

**Objetivo:** Comparar cómo cambia una respuesta cuando se utiliza un prompt general y cuando se proporcionan instrucciones específicas y organizadas.

**Actividad 1: Prompt vago**

En un chat nuevo de ChatGPT se envió el siguiente prompt:

```text
Hazme una descripcion de un sistema de biblioteca.
```

**Resultado obtenido:**

ChatGPT generó una descripción general de un sistema de biblioteca. Explicó que su objetivo es facilitar la administración y organización de los recursos bibliográficos de una institución.

También mencionó diferentes usuarios, como estudiantes, docentes y bibliotecarios, y describió siete funcionalidades: registro de libros, gestión de usuarios, préstamo de libros, devolución, búsqueda, control de inventario y generación de reportes.

La respuesta terminó explicando que un sistema de biblioteca permite modernizar la administración de los recursos bibliográficos y mejorar la atención a los usuarios.

**Actividad 2: Prompt estructurado**

En otro chat nuevo se envió el siguiente prompt:

```text
Actúa como analista de sistemas. Redacta una descripcion breve de un sistema web para gestionar prestamos de libros en una biblioteca. Incluye objetivo, usuarios principales y 3 funcionalidades clave. Utiliza un lenguaje claro y profesional y presenta el resultado en 3 parrafos.
```

**Resultado obtenido:**

El sistema web para gestionar préstamos de libros en una biblioteca tiene como objetivo automatizar y optimizar el proceso de préstamo y devolución de libros, facilitando el control del inventario bibliográfico y mejorando la atención a los usuarios. Además, permite mantener un registro organizado y actualizado de las operaciones realizadas en la biblioteca.

Los usuarios principales del sistema son los administradores o bibliotecarios, encargados de gestionar los libros, registrar préstamos y controlar las devoluciones, y los lectores o estudiantes, quienes podrán consultar el catálogo disponible y revisar sus préstamos activos.

El sistema contará con tres funcionalidades clave: 1) Gestión del catálogo de libros, que permitirá registrar, modificar, eliminar y consultar libros; 2) Gestión de préstamos y devoluciones, que facilitará el registro de préstamos, fechas de entrega y devoluciones; y 3) Control de usuarios y consultas, que permitirá administrar los datos de los lectores, consultar su historial de préstamos y verificar la disponibilidad de los libros.

**Actividad 3: Comparación de resultados**

| Criterio | Prompt vago | Prompt estructurado |
|---|---|---|
| Menciona el objetivo del sistema | Sí | Sí |
| Menciona a los usuarios principales | Sí | Sí |
| Tiene exactamente 3 funcionalidades | No | Sí |
| Está en 3 párrafos | No | Sí |
| Lo usaría en un informe real | No | Sí |

**Análisis:**

El prompt vago produjo una respuesta general y extensa, con siete funcionalidades y diferentes explicaciones sobre el sistema de biblioteca. Aunque presentó información útil, no indicó una cantidad específica de funcionalidades ni una estructura determinada.

En cambio, el prompt estructurado permitió obtener una respuesta más precisa y organizada, porque indicó el rol que debía asumir ChatGPT, el objetivo, los usuarios principales, exactamente tres funcionalidades y la cantidad de párrafos.

**Reflexión:**

Este ejercicio demuestra que un prompt estructurado permite controlar mejor el contenido y la presentación de una respuesta. Cuanto más claras y específicas son las instrucciones, más fácil es obtener un resultado que cumpla con lo solicitado y pueda utilizarse en un informe.

**Captura del resultado:**

Colocar aquí la captura de las dos respuestas, lado a lado.

### 3.5 Ejercicio 5: Anatomía de un prompt, paso a paso

**Objetivo:** Comprender cómo mejora una respuesta al agregar progresivamente componentes a un prompt: rol, contexto, instrucción, ejemplos y formato.

**Herramientas utilizadas:** ChatGPT y Java.

**Actividad 1: Enviar los cinco niveles del prompt**

Se realizaron cinco pruebas en chats nuevos de ChatGPT. En cada nivel se conservó el prompt anterior y se agregó una nueva instrucción.

**Nivel 1: Prompt básico**

```text
Crea un programa en Java.
```

**Resultado obtenido:**

ChatGPT respondió que podía crear un programa en Java y preguntó qué tipo de programa se necesitaba. También presentó varios ejemplos, como una calculadora, un sistema de ventas, un sistema de notas, un inventario, un registro de usuarios y un sistema de biblioteca.

**Nivel 2: Agregar el rol**

```text
Actúa como desarrollador Java. Crea un programa en Java.
```

**Resultado obtenido:**

ChatGPT asumió el rol de desarrollador Java. Indicó que podía ayudar a crear un programa funcional, con código limpio, organizado y comentado. También preguntó qué tipo de programa se deseaba desarrollar y presentó diferentes alternativas.

**Nivel 3: Agregar el contexto**

```text
Actúa como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda.
```

**Resultado obtenido:**

ChatGPT propuso desarrollar un sistema de gestión de productos para una tienda utilizando Java y programación orientada a objetos (POO).

También presentó funcionalidades como registrar productos, mostrar productos, buscar por código, actualizar información, eliminar productos, modificar el stock y calcular el valor total del inventario.

**Nivel 4: Agregar la instrucción específica**

```text
Actúa como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. Crea una clase llamada Producto con cuatro atributos: codigo, nombre, precio y cantidad.
```

**Resultado obtenido:**

ChatGPT explicó la estructura de la clase `Producto` y describió sus cuatro atributos:

- `codigo`: identificador del producto, de tipo `int`.
- `nombre`: nombre del producto, de tipo `String`.
- `precio`: precio del producto, de tipo `double`.
- `cantidad`: unidades disponibles, de tipo `int`.

También presentó el código Java con un constructor, métodos getters y setters y un método `mostrarProducto()` para visualizar los datos.

**Nivel 5: Agregar el formato de respuesta**

```text
Actúa como desarrollador Java. Crea un programa en Java para gestionar los productos de una tienda. Crea una clase llamada Producto con cuatro atributos: codigo, nombre, precio y cantidad. Antes de mostrar el código, explica brevemente la estructura de la clase y la función de cada atributo. Después, presenta el código Java completo en un bloque de código.
```

**Resultado obtenido:**

ChatGPT presentó primero una explicación de la estructura de la clase `Producto`, indicando la función de cada uno de sus cuatro atributos.

Después, explicó que la clase tendría un constructor para inicializar los atributos, métodos getters y setters para consultar y modificar los datos y un método `mostrarProducto()` para visualizar la información.

Finalmente, presentó el código Java completo de la clase `Producto` y una clase principal `Main`, que crea tres productos de ejemplo: Laptop, Mouse y Teclado, y muestra sus datos en pantalla.

**Actividad 2: Comparación de los cinco niveles**

| Nivel | Componente agregado | Resultado obtenido |
|---|---|---|
| 1 | Prompt básico | Solicitud general y pregunta sobre el tipo de programa. |
| 2 | Rol | ChatGPT asume el papel de desarrollador Java. |
| 3 | Contexto | Se define que el programa gestionará productos de una tienda. |
| 4 | Instrucción | Se especifica la clase Producto y sus cuatro atributos. |
| 5 | Formato | Se solicita explicar la estructura antes de presentar el código completo. |

**Actividad 3: Análisis**

En el primer nivel, el prompt fue muy general y ChatGPT necesitó preguntar qué tipo de programa se deseaba crear. Al agregar el rol de desarrollador Java, la respuesta se orientó hacia la programación en ese lenguaje.

En el tercer nivel, el contexto permitió definir el propósito del programa: gestionar los productos de una tienda. En el cuarto nivel, la instrucción específica indicó la clase que debía crearse y sus cuatro atributos.

Finalmente, en el quinto nivel, se indicó cómo debía organizarse la respuesta: primero explicar la estructura de la clase y la función de cada atributo y después presentar el código Java completo. Esto permitió obtener una respuesta más ordenada y útil para comprender el programa.

**Reflexión sobre la anatomía de un prompt**

Este ejercicio demuestra que un prompt efectivo se construye agregando información de manera progresiva. El rol define quién debe ser la IA, el contexto proporciona información sobre el problema, la instrucción indica qué debe realizar, los ejemplos ayudan a orientar el resultado y el formato establece cómo debe presentarse.

Por lo tanto, cuanto más completo y organizado sea el prompt, mayor será la posibilidad de obtener una respuesta clara, específica y adecuada a lo solicitado.

**Capturas del resultado:**

Colocar las capturas de los cinco niveles en orden, desde el nivel 1 hasta el nivel 5. Incluir especialmente la respuesta final con la explicación de la clase `Producto` y el código Java completo.

## 4. Conclusiones generales

- La claridad de las instrucciones influye directamente en la calidad de las respuestas generadas por una herramienta de inteligencia artificial.
- Los tokens permiten comprender cómo los modelos procesan los textos y cómo la información de una conversación forma parte de su contexto.
- La temperatura influye en la variabilidad de los resultados: los valores bajos favorecen respuestas más predecibles y los valores altos permiten mayor diversidad.
- Los prompts estructurados permiten obtener respuestas más precisas, organizadas y ajustadas a los requisitos solicitados.
- La combinación de rol, contexto, instrucciones y formato ayuda a construir prompts más completos y efectivos.

## 5. Reflexión final

Durante el desarrollo del laboratorio pude comprobar que la ingeniería de prompts es importante para aprovechar correctamente las herramientas de inteligencia artificial. Aprendí que no basta con realizar una pregunta general, sino que es necesario proporcionar instrucciones claras, contexto y un formato esperado.

También comprendí que experimentar con diferentes prompts permite comparar resultados, identificar mejoras y obtener respuestas más útiles para resolver problemas de programación y otras actividades académicas.