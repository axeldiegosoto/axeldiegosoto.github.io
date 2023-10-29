---
title: Sentencia If, If-Else y Else-If
date: 2023-10-28 12:00:00 0
categories: [programacion, java]
tags: [java, programacion, sentencias de control, condicionales, sentenciaif, metodos de entrada, ifelse, elseif]
---
> Nota: TODO el código de este artículo supone que esta dentro de la función main.
{: .prompt-warning }

## ¿Qué la sentencia IF?
La sentencia if es una sentencia de control la cual nos permite ejecutar o no un bloque de código en caso de que se cumpla una condición.
### Estructura
```
if(condición){
    // Bloque de instrucciones
}
```
> La condición representa un valor booleano, puede ser una variable tipo `boolean` como tal, o puedes hacer uso de los operadores relacionales y lógicos.
{: .prompt-info }

### Ejemplo en Java
#### Si la condición se cumple
```java
boolean jugadorActivo = true;

if(jugadorActivo){
    System.out.println("Eres un jugador Activo");
}
```
```shell
Eres un jugador Activo
```
#### Si la condición no se cumple
```java
int edad = 15;

if(edad >= 18){
    System.out.println("Eres mayor de edad");
}
```
> En caso de que la condición no se cumpla, no se imprimirá el mensaje.
{: .prompt-info }

## La sentencia If-Else
Ahora bien, anteriormente vimos que con el `if`, el código se ejecutaba o no se ejecutaba, en el caso del **if-else** pasa algo distinto, veamos primero la estructura.
### Estructura
```
if(condición){
    // Bloque de instrucciones
}else {
    // Bloque de instrucciones
}
```
Notamos que seguimos teniendo la sentencia if y la condición, la única diferencia es que ahora el if está seguido por un else y otro bloque de instrucciones. La sentencia if funciona de la misma manera, o se ejecuta o no se ejecuta depende si la condición es `true`, pero ahora en caso de que la condición sea `false` se ejecutará el bloque de instrucciones del `else`. Entonces ahora tenemos que bien o se ejecuta el `if` o se ejecuta el `else`, pero siempre alguno de los dos se tiene que ejecutar.

### Ejemplo en Java
#### Cuando se cumple la condición
```java
int edad = 21;

if(edad >= 18){
    System.out.println("Eres mayor de Edad");
}else {
    System.out.println("Eres menor de Edad");
}
```
```shell
Eres mayor de Edad
```
#### Si no se cumple la condición
```java
boolean jugadorActivo = false;

if(jugadorActivo){
    System.out.println("Eres un jugador activo");
}else {
    System.out.println("NO eres un jugador activo");
}
```
```shell
NO eres un jugador activo
```
> Con la sentencia If-Else notamos que o bien se ejecuta el bloque de instrucciones del `if` o **sino** se ejecuta el bloque de instrucciones del `else`.
{: .prompt-info }

## Sentencia Else-If
Esta sentencia es la combinación de las dos mencionadas en la parte de arriba y debe de tener un If antes obligatoriamente y opcionalmente puede ir después el else, veamos un ejemplo con solo un If y un else:
```java
float estatura = 1.70f;

if(estatura >= 1.80){
    System.out.println("Eres alto");
}else {
    System.out.println("Eres chaparro");
}
```
Este ejemplo me dice que si mido 1.80 o más soy una persona alta y sino soy una persona chaparra, pero como puedo manejar un **tercer caso**, en este ejemplo quiero que también me diga si tengo estatura promedio, entonces hacemos unas modificaciones:
```java
float estatura = 1.70f;

if(estatura >= 1.80){
    System.out.println("Eres alto");
}else if(estatura >= 1.70){ // Sentencia Else-If
    System.out.println("Tienes estatura promedio");
}else {
    System.out.println("Eres chaparro");
}
```
> Aquí ya agregamos una sentencia Else-If y esta sentencia también debe de tener su condición, y si la condición es `true` se ejecutará el bloque de instrucciones del Else-If.
{: .prompt-info }

### Cosas a tener en cuenta
#### Podemos tener el número de Else-If que querramos
Dado cualquier caso que puedas tener puedes hacer uso de los Else-If infinitamente, por ejemplo:
```java
float estatura = 1.70f;

if(estatura >= 1.90){
    System.out.println("Eres muy alto");
}else if(estatura >= 1.80){
    System.out.println("Eres alto");
}else if(estatura >= 1.70){
    System.out.println("Tienes estatura promedio");
}else if(estatura >= 1.60){
    System.out.println("Eres chaparro");
}else {
    System.out.println("Eres muy chaparro");
}
```
Dado estas modificaciones manejamos 5 casos distintos de nuestro programa, pero podemos tener los que nosotros querramos.

#### Las condiciones se realizan en orden de arriba hacia abajo
Podemos observar que en el código de arriba puede que nuestro valor de estatura sea `true` en mas de una condición, pero tomando en cuenta que se realizan de una en una y arriba hacia abajo, se ejecuta la primera que retorne `true` en la condición, por ende, el código y lo que nos muestra sería así:
```java
float estatura = 1.70f;

if(estatura >= 1.90){ // Retorna false
    System.out.println("Eres muy alto");
}else if(estatura >= 1.80){ // Retorna false
    System.out.println("Eres alto");
}else if(estatura >= 1.70){ // Retorna true
    System.out.println("Tienes estatura promedio");
}else if(estatura >= 1.60){ // Retorna true pero ya no se ejecuta
    System.out.println("Eres chaparro");
}else {
    System.out.println("Eres muy chaparro");
}
```
```shell
Tienes estatura promedio
```
> Teniendo en cuenta que tenemos este tipo de sentencias juntas, podemos observar que en cualquier tipo de caso siempre se nos va a ejecutar un bloque de instrucción.
{: .prompt-info }

## Ejercicio propuesto
Si quieres afianzar tus habilidades con estas sentencias puedes ver mi ejercicio de un piedra, papel y tijeras aquí mismo en mi blog:
<https://axeldiegosoto.github.io/posts/piedra-papel-tijeras-java/>