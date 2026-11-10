# Tarea: Mi prompt profesional

## Funcionalidad elegida

La funcionalidad elegida es el registro de productos de una tienda mediante un programa de consola desarrollado en Java.

El programa utiliza programación orientada a objetos. Cada producto contiene cuatro atributos: código, nombre, precio y cantidad. Se eligió esta funcionalidad porque permite aplicar clases, objetos, constructores, encapsulamiento, getters, setters y validaciones.

## Versión 1: prompt básico

**Prompt utilizado:**

```text
Crea un programa en Java para registrar productos de una tienda.
```

**Resultado obtenido:**

ChatGPT generó una propuesta general para desarrollar un programa en Java que permite registrar productos de una tienda. Presentó una explicación de las funcionalidades principales y una propuesta de código.

**¿Qué faltaba?**

- No especificaba los atributos de cada producto.
- No indicaba las clases que debía utilizar.
- No solicitaba validaciones.
- No establecía el formato de presentación.

**Análisis:**

Esta versión permitió obtener una idea general, pero sus instrucciones eran demasiado amplias. Fue necesario agregar requisitos para conseguir una solución más completa.

## Versión 2

**Prompt utilizado:**

```text
Actúa como desarrollador Java. Crea un programa para registrar productos de una tienda. Cada producto debe tener código, nombre, precio y cantidad. Utiliza una clase llamada Producto y una clase principal Main. Incluye un ejemplo de ejecución.
```

**Resultado obtenido:**

ChatGPT presentó una solución organizada en dos clases: `Producto` y `Main`. Incluyó los atributos solicitados, una explicación de las clases y un ejemplo de ejecución.

**¿Qué mejoró?**

- Se estableció el rol de desarrollador Java.
- Se especificaron los cuatro atributos del producto.
- Se indicaron las dos clases del programa.
- Se solicitó un ejemplo de ejecución.
- La respuesta obtuvo una estructura más clara.

**¿Qué todavía faltaba?**

No se especificaron los tipos de datos, los atributos privados, los métodos getters y setters ni las validaciones necesarias.

**Análisis:**

La segunda versión produjo una respuesta más organizada y específica. Sin embargo, todavía era necesario definir los requisitos técnicos del programa.

## Versión 3: prompt final

**Prompt utilizado:**

```text
Actúa como desarrollador Java especializado en programación orientada a objetos.

Desarrolla un programa de consola para registrar productos de una tienda.

Cada producto debe tener cuatro atributos: codigo (int), nombre (String), precio (double) y cantidad (int). Crea una clase llamada Producto con atributos privados, un constructor, métodos getters y setters, y un método mostrarProducto().

En la clase principal Main, crea tres objetos Producto con los siguientes datos de ejemplo:
- Código: 101, nombre: Laptop, precio: 2500.00, cantidad: 5.
- Código: 102, nombre: Mouse, precio: 45.50, cantidad: 20.
- Código: 103, nombre: Teclado, precio: 85.00, cantidad: 15.

Valida que el precio sea mayor que cero y que la cantidad no sea negativa. Utiliza nombres claros, código ordenado y comentarios breves.

Antes del código, explica la estructura de las clases y la función de cada una.

Presenta el código completo de Producto.java y Main.java en bloques separados de Java.

Después, incluye los pasos para compilar y ejecutar el programa desde la terminal, un ejemplo del resultado esperado en consola, una tabla que explique los conceptos de programación orientada a objetos utilizados y una conclusión breve.

Utiliza un lenguaje claro y profesional. No omitas los métodos solicitados ni las validaciones.
```

**Resultado obtenido:**

ChatGPT presentó una solución organizada en dos archivos: `Producto.java` y `Main.java`.

La clase `Producto` contiene cuatro atributos privados, un constructor, métodos getters y setters y el método `mostrarProducto()`. También incorpora validaciones para impedir precios iguales o menores que cero y cantidades negativas.

La clase `Main` crea tres objetos con los siguientes datos:

| Código | Producto | Precio | Cantidad |
|---:|---|---:|---:|
| 101 | Laptop | S/ 2500.00 | 5 |
| 102 | Mouse | S/ 45.50 | 20 |
| 103 | Teclado | S/ 85.00 | 15 |

La respuesta también incluyó la estructura de los archivos, explicación del código, instrucciones de compilación y ejecución y un ejemplo de salida en consola.

**¿Qué mejoró respecto a la versión anterior?**

- Se definieron los tipos de datos de cada atributo.
- Se solicitó encapsulamiento mediante atributos privados.
- Se especificaron los getters, setters y `mostrarProducto()`.
- Se agregaron validaciones para el precio y la cantidad.
- Se proporcionaron tres objetos con datos concretos.
- Se estableció el formato de presentación de la respuesta.
- Se solicitaron instrucciones para compilar y ejecutar el programa.

**Análisis:**

La tercera versión permitió obtener una solución más completa porque especificó el rol, las instrucciones, el contexto técnico, los ejemplos y el formato esperado. De esta manera, la respuesta se ajustó mejor a los requisitos del ejercicio.

## Componentes del prompt final

El prompt final utiliza los cinco componentes solicitados:

| Componente | Parte del prompt | Función |
|---|---|---|
| Rol | Actúa como desarrollador Java especializado en programación orientada a objetos. | Define el perfil que debe asumir el modelo. |
| Instrucción | Desarrolla un programa de consola para registrar productos de una tienda. | Indica la tarea principal. |
| Contexto | Define los atributos, las clases, los métodos y las validaciones. | Proporciona los requisitos técnicos. |
| Ejemplos | Crea tres objetos Producto con datos concretos de ejemplo. | Orienta la solución mediante datos específicos. |
| Formato | Presenta los archivos separados, pasos de ejecución, tabla y conclusión. | Organiza la presentación de la respuesta. |

## Evaluación del resultado

Se evaluó la respuesta generada por ChatGPT utilizando los siguientes criterios:

| Criterio de evaluación | Sí | No |
|---|:---:|:---:|
| Define las clases Producto y Main. | X | |
| Utiliza los cuatro atributos solicitados con sus tipos de datos. | X | |
| Incluye constructor, getters y setters. | X | |
| Valida que el precio sea mayor que cero y que la cantidad no sea negativa. | X | |
| Crea tres objetos y muestra su información. | X | |
| Presenta los archivos de código por separado. | X | |
| Incluye instrucciones de compilación y ejecución. | X | |

**Análisis de la evaluación:**

La respuesta final cumplió con los criterios establecidos. Se obtuvo una solución organizada en dos clases, con atributos privados, métodos de acceso, validaciones y tres objetos de ejemplo.

La evaluación permitió comprobar que la versión final del prompt proporcionó instrucciones suficientes para orientar la respuesta hacia el resultado esperado.

## Errores que evité

### Error 1: Ser demasiado general

Un prompt demasiado general puede producir respuestas que no cumplen todos los requisitos de una actividad.

**Cómo lo evité:**

En la primera versión solamente solicité crear un programa para registrar productos. En las siguientes versiones agregué los atributos, las clases, los métodos y las validaciones necesarias para obtener una solución más específica.

### Error 2: No indicar el formato de respuesta

Cuando no se establece cómo presentar la solución, la respuesta puede no tener la organización necesaria para comprender o utilizar el código.

**Cómo lo evité:**

En la tercera versión indiqué que el código debía presentarse en dos bloques separados, uno para `Producto.java` y otro para `Main.java`. También solicité la estructura del proyecto, los pasos de ejecución, una tabla explicativa y una conclusión.