---
title: Variables en Java
date: 2023-08-25 10:00:00 0
categories: [programacion, java]
tags: [java, software, programacion, fundamentos de programacion, variables, tipos de datos]
---

## Variables

Las variables las usamos para asociar información a ellas para manejarlas, darles un nombre, actualizar un valor, usarla en operaciones, etc. Las variables tienen muchas funciónes y siempre están en nuestros programas, les muestro un ejemplo de una variable en java:

```java
package variables;

public class Variables {

    public static void main(String[] args) {
        // Nuestra variable
        int edad = 18;
    }
    
}
```

### Partes de una variable

Las partes de la definición de una variable son:
* El **tipo**, en este caso nuestro tipo es `int` (tipos de datos).
* El **identificador**, nuestro identificador es `edad`, este nos ayuda a llamarlo dentro de nuestro programa con ese identificador o a reasignar un nuevo valor.
* El **operador de asignación** `=`, con este le indicamos al programa que el siguiente dato es el valor que tendrá nuestra variable.
* El **valor**, en nuestro caso usamos `18`, este valor tiene que ser compatible con el tipo de dato de la variable.

## Tipos de datos

### Tipos de datos primitivos
A continuación te mostraré tablas clasificadas por cada tipo de dato primitivo, con su valor de almacenamiento y los valores que puede almacenar:

##### Numéricos enteros

|tipo       |Valor de Almacenamiento |Rango de valores   |
|:---------:|:----------------------:|:-----------------:|
|`byte`     |1 byte                  |[`-128`, `127`]        |
|`short`    |2 bytes                 |[`-32768`, `32767`]  |
|`int`      |4 bytes                 |[`-2147483648`, `2147483647`]|
|`long`     |8 bytes                 |[`-9223372036854775808`, `9223372036854775807`]        |

##### Numéricos en punto flotante

Existen dos tipos de datos primitivos que pueden almacenar valores de punto flotante,son los siguientes:

|tipo       |Valor de Almacenamiento |
|:---------:|:----------------------:|
|`float`     |32 bits                |
|`double`    |64 bits                |

EL tipo  `float` se le denomina de **precisión simple**, puede almacenar valores decimales pero de una forma menos precisa que el tipo `double`. Ambos tipos pueden almacenar números muy grandes.

##### Booleanos y caracteres

|tipo       |Valor de Almacenamiento |Valores posibles|
|:---------:|:----------------------:|:--------------:|
|`boolean` |16 bits                  |`true` / `false`|
|`char`    |16 bits                  |**caracteres ASCII**|