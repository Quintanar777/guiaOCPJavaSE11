## Creando un simple programa en java

### El metodo main

Las clases java no son **ejecutables**. Tu no puedes **ejecutar** clases Java. La Java Virtual Machine(JVM) es un ejecutable. Tu ejecutas la JVM

El metodo que la JVM esta programado para buscar en la clase es llamado **el metodo "main"** y este metodo tiene una muy especifica firma:

- Su nombre debe ser **main**
- Debe recibir especificamente un parametro de tipo **String array**
- Debe retornar **void**
- Debe ser **public** y **static**

Es libre de declarar cualquier exception en la clausula **throws**

#### Ejemplos de metodos **main** validos:

```java
public static void main (String[] args) {}
```
Esta es la versión que tu veras mas comunmente.

```java
public static void main (String... args) {}
```
Nota que **String...** es lo mismo que **String[]** en lo que respecta en la JVM

```java
public static void main (String... args) throws Exception { throw new Exception(); }
```
El metodo main tiene permitido a lanzar cualquier exception

#### Ejemplos de metodos **main** invalidos:

```java
static void main (String... args) { }
```
Es invalido porque no es **public**

```java
public void main (String... args) { }
```
Es invalido porque no es **static**

```java
public void main (String[] a, String[] b) { }
```
Es invalido porque no toma exactamente un parametro de tipo String array

```java
static void Main (String[] args) { }
```
Es invalid porque no es public y el nombre inicia con M mayuscula, recuerda que Java es case sensitive

### Argumentos de linea de comandos