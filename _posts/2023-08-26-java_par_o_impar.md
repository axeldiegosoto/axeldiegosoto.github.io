---
title: Clasificar pares e impares en Java
date: 2023-08-26 09:00:00 0
categories: [programacion, java]
tags: [java, programacion, ejercicios, condicionales, sentenciaif, operadores lógicos]
---

# Aprende a usar el operador módulo con un ejercicio sencillo

En este tutorial vamos a realizar un programa que me permita ingresar un número el cual posteriormente lo vamos a procesar mediante una condición para que nos muestre por consola si ese número es par o impar.

### Definimos nuestras variables

Como primer punto definiremos nuestras variables, dadas las circunstancias del problema planteado solo necesitaremos dos variables (podemos añadir más durante el proceso):

1. Variable tipo `int` que almacenara el número que le pasemos por el *Scanner* que llamaremos **numero**

2. Variable tipo `Scanner` que llamaremos **entrada**

```java
package parimpar;

// Importamos el modulo Scanner
import java.util.Scanner;

public class ParImpar {

    public static void main(String[] args) {
        // Definimos las variables aquí de esta forma
        Scanner tec = new Scanner(System.in);
        int numero;
    }
    
}
```
> Noten que aún no le asignamos valor a la variable `int numero`.
{: .prompt-info }

### Asignamos valor al número

Con el uso del Scanner asignamos el valor del número:

```java
public static void main(String[] args) {
    Scanner tec = new Scanner(System.in);
    int numero;

    // Imprimimos un mensaje y asignamos el valor
    System.out.println("Digite un número:");
    numero = tec.nextInt();
}
```

### Verificamos si el número es par

Para hacerlo, lo único que tenemos que hacer es usar el operador módulo, lo usamos para dividir el número entre 2 y gracias al operador solo nos puede dar dos resultados diferentes que sería: el 0 y el 1.

| Si el resultado es 0 | Si el resultado es 1 |
|:---------------------|:---------------------|
| El número es par     | El número es impar   |

#### Pongamoslo en práctica

```java
public static void main(String[] args) {
    Scanner tec = new Scanner(System.in);
    // Añadimos la variable verificacion
    int numero, verificacion;

    System.out.println("Digite un número:");
    numero = tec.nextInt();

    // Asignamos un valor a la variable verificacion
    verificacion = numero % 2;

    // Y por último podemos imprimir el mensaje para probarlo
    System.out.println("El resultado es: " + verificacion);
}
```

> Solo puede haber dos valores posibles en el resultado.
{: .prompt-tip }

#### Si es par

```bash
Digite un número:
10
El resultado es: 0
```

#### Si es impar

```bash
Digite un número:
15
El resultado es: 1
```

### Mostrar si es par o impar

Por último, solo tenemos que usar una condición para mostrar si es un número par o impar, haciendo esto ya no es necesario mostrar el resultado de la verificación así que lo quitamos. Quedaría de esta forma:

```java
public static void main(String[] args) {
    Scanner tec = new Scanner(System.in);
    int numero, verificacion;
    
    System.out.println("Digite un número:");
    numero = tec.nextInt();
    
    
    verificacion = numero % 2;
    
    // Añadimos la condición
    // Si es par
    if(verificacion == 0){
        System.out.println("Su número es PAR");
    }else {
    // En caso de que no se cumpla la condición suponemos que es impar
        System.out.println("S número es IMPAR");
    }        
}
```

#### Ejecución

```bash
Digite un número:
32
Su número es PAR
```

```bash
Digite un número:
15
Su número es IMPAR
```

### Conclusión

Y listo, así tenemos un sencillo programa en el que ponemos los fundamentos a prueba, si no le entiendes a algunos conceptos en los siguientes días estaré subiendo contenido relacionado a conceptos usados en este programa pero de forma mas específica, así que espero verte pronto, bye.

