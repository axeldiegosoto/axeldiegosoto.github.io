---
title: Como hacer un Piedra, Paper y Tijeras en Java
date: 2023-08-27 12:00:00 0
categories: [programacion, java]
tags: [java, programacion, ejercicios, condicionales, sentenciaif, metodos de entrada]
---

## Modalidad de 2 jugadores

### Preparar el programa

Para este programa estaremos utilizando el IDE llamado netbeans y crearemos un nuevo proyecto java llamado **PiedraPapelYTijeras**.

![Desktop View](/assets/img/posts/2023-08-27-piedra-papel-tijeras-java/screenshot_006.png){: width="972" height="589"}
![Desktop View](/assets/img/posts/2023-08-27-piedra-papel-tijeras-java/screenshot_007.png){: width="972" height="589"}

Una vez teniendo un proyecto nuevo y limpio podemos empezar con lo básico, que sería definir nuestras variables del programa.

Como primer caso podríamos crear dos variables que serían el jugador1 y el jugador2, ambas variables serán objetos de tipo String ya que alamacenarán las opciones `"piedra"`, `"papel"` y `"tijeras"`.

```java
package piedrapapelytijeras;

public class PiedraPapelYTijeras {

    public static void main(String[] args) {
        // Nuestras variables
        String jugador1, jugador2;
    }
    
}
```

Para darles valor a nuestras variables usaremos el modulo `Scanner` que nos habilita la opción de ingresar datos mediante el teclado.

```java
package piedrapapelytijeras;

// Importamos el modulo
import java.util.Scanner;

public class PiedraPapelYTijeras {

    public static void main(String[] args) {
        // Y agregamos la variable de esta forma
        Scanner tec = new Scanner(System.in);
        String jugador1, jugador2;
    }
    
}
```

### Ingresar datos de los jugadores

Si bien podemos tan solo pedir los datos de los jugadores de esta forma:

```java
public static void main(String[] args) {
    Scanner tec = new Scanner(System.in);
    String jugador1, jugador2;
    
    // Almacenamos los datos mediante el Scanner
    System.out.println("Jugador 1:");
    jugador1 = tec.nextLine();
    
    System.out.println("Jugador 2:");
    jugador2 = tec.nextLine();
}
```

De esta forma así nada más, los datos se guardarían sin problemas, el único problema es que podemos ingresar cualquier dato que sea un `String`, y nosotros tan solo estamos buscando que los jugadores ingresen los datos `"piedra"`, `"papel"` y `"tijeras"`. Entonces tendríamos que validar los datos.

### Validar los datos

Para validar los datos necesitaremos un bucle `do while` y dentro de este bucle estarán las instrucciones para almacenar los datos de los jugadores, también necesitaremos definir una variable de tipo `boolean` que se llamará `bandera` para poder decirle al programa si los datos son validos, de esta forma:

| Boolean | `true`   | `false`  |
|:--------|---------|--------|
|`bandera`    | Los datos son válidos| Los datos son inválidos|

```java
do {
    if(!bandera){
        System.out.println("Datos inválidos");
    }
    
    System.out.println("Jugador 1:");
    jugador1 = tec.nextLine();
    
    if(jugador1.equals("piedra") || jugador1.equals("papel") || jugador1.equals("tijeras")){
        bandera = true; 
    }else {
        bandera = false;
        continue;
    }

    System.out.println("Jugador 2:");
    jugador2 = tec.nextLine();
    
    if(jugador2.equals("piedra") || jugador2.equals("papel") || jugador2.equals("tijeras")){
        bandera = true; 
    }else {
        bandera = false;
        continue;
    }
}while(!bandera);
```