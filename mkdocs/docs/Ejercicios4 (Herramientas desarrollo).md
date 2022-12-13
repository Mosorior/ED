# EJERCICIOS 4

## 1. Ejecuta el programa "Hola mundo" en los siguientes lenguajes:
### bash
```bash
#!/bin/bash

echo "Hello World"

exit 0
```


### python

```python
print("Hello World")
```

### php

```php
<?php
echo "Hello World";
?>
```

### javascript

```javascript
<script>
    alert('Hello World');
</script>
```

### c

```c
#include <stdio.h>
int main(){
    printf("Hello World");
    return 0;
}
```

### c++

```c++
#include <iostream>
int main(){
    cout<<"Hello World";
    return 0;
}
```

### java

```java
class HelloWorld {
    public static void main(string[] args){
        System.out.println("Hello World");
    }
}
```

### ruby

```ruby
Archivo: hello_world.ruby
    puts "Hello World"
```



### go

```go
package main

import "fmt"
func main(){
    fmt.println("Hello World")
}
```

Terminal

```bash
$ go run hello-world.go

$ go build hello-world.go
$ ls

$ ./hello-world
```

### rust

```rust
fn main(){
    println!("Hello World);
}
```

### lisp

```lisp
(format t "Hello, World!")
```

### ensamblador (nasm)

Código fuente:

```
SECTION .DATA
	hello:     db 'Hello world!',10
	helloLen:  equ $-hello

SECTION .TEXT
	GLOBAL _start 

_start:
	mov eax,4            ; 'write' system call = 4
	mov ebx,1            ; file descriptor 1 = STDOUT
	mov ecx,hello        ; string to write
	mov edx,helloLen     ; length of string to write
	int 80h              ; call the kernel



mov eax,1            ; 'exit' system call
mov ebx,0            ; exit with error code 0
int 80h              ; call the kernel
```

Compilación:

    #Compilación
    nasm -f elf64 hola.asm -o hola.o
    
    #Enlace
    ld hola.o -o hola
    
    #Ejecución
    ./hola


## 2. Para cada uno de los lenguajes anteriores, indica el proceso realizado para conseguir ejecutar el código: ¿compilación o interpretación?

- bash: interpretado
- python: interpretado
- php: interpretado
- javascript (nodejs): interpretado
- c: compilado
- c++: compilado
- java: compilado
- ruby: interpretado
- go: compilado
- rust: compilado
- lisp: interpretado

## 3. Para cada uno de los lenguajes anteriores, indica el nombre del compilador o interprete utilizado en GNU/Linux.

- bash: Terminal/Consola
- python: python IDE
- php: php
- javascript (nodejs): java
- c: gcc
- c++: gcc
- java: jdk
- ruby: yarv
- go: go
- rust: rustc
- lisp: lisp

## 4. Investiga y averigua que extensión tienen los archivos de código fuente de los siguientes lenguajes:

- bash: .sh
- python: .py
- php: .php
- javascript: .js
- c: .c
- c++: .C
- java: .java
- ensamblador: .ASM
- ruby: .ruby
- go: .GO
- rust: .rs
- lisp: .lsp

## 5. Scripts ejecutables para los lenguajes interpretados. Edita los scripts para los siguientes lenguajes:

- bash: 
- python: 
- php: 
- javascript: 
- java: 
- ruby: 
- go: 
- rust: 
- lisp: 

Ya está hecho en Ej 1

## 6. ¿Qué extensión tienen los archivos de código objeto?
.obj

## 7. Lenguaje C. Código en varios archivos. Obtener el código objeto a partir del código fuente de los 3 archivos siguientes:

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej7.png)

## 8. Lenguaje C. Código en varios archivos. Obtener el código binario ejecutable a partir del código objeto de los 3 archivos anteriores:

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej7.png)

## 9. Lenguaje C++. Código en varios archivos. Obtener el código objeto a partir del código fuente de los 3 archivos siguientes:
![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej9.png)

## 10. Lenguaje C++. Código en varios archivos. Obtener el código binario ejecutable a partir del código objeto de los 3 archivos anteriores:
![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej10.png)

## 11. Bibliotecas. Define que se entiende por biblioteca o librería y los tipos que existen.
Son un conjunto de archivos que se utiliza para desarrollar software. Su fin es ser utilizada por otros programas de forma autónoma.

## 12. Bibliotecas. ¿Qué tipo es el más utilizado actualmente? ¿Por qué?
Las bibliotecas dinámicas porque son menos pesadas y el programa se beneficia de sus actualizaciones.

## 13. Bibliotecas. Crea una biblioteca dinámica en C que proporcione las funciones para sumar, restar, multiplicar y dividir 2 números enteros. Crea un programa que haga uso de ella y comprueba que se ejecuta correctamente.

Creamos el archivo aritmetica.c con el siguiente código:

```c
#include <stdio.h>
#include <stdlib.h>
int suma (int a, int b){
    return a+b;
}
int resta (int a, int b){
   return a-b;
}
int multiplicar (int a, int b){
   return a*b;
}
int dividir (int a, int b){
   return a/b;
}
```

Convertimos a libreria:

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej13.png)

## 14. Bibliotecas. Crea una biblioteca dinámica en Java que proporcione las funciones para sumar, restar, multiplicar y dividir 2 números enteros. Crea un programa que haga uso de ella y comprueba que se ejecuta correctamente.

Creamos el archivo aritmetica.java con el siguiente código:

```java
public class aritmetica{

​    public int suma(int a, int b){

​        return a+b;

​    }

​    public int resta(int a, int b){

​        return a-b;

​    }

​    public int multiplicar(int a, int b){

​        return a*b;

​    }

​    public int dividir(int a, int b){

​        return a/b;

​    }

}
```

Convertimos a librería:

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej14.png)



## 15. Bibliotecas. Busca información y explica las ventajas y desventajas de usar bibliotecas estáticas.

Las bibliotecas estáticas dan la seguridad de que todas las dependencias están en la aplicación y con su versión correcta. Esto evita problemas de dependencia. También permite que la aplicación se contenga dentro de un solo archivo ejecutable, simplificando la distribución y la instalación.

Las estáticas son más eficientes que las dinámicas, pues solo se cargan las bibliotecas necesarias y no todas.

Algunas desventajas de las estáticas es que al almacenarse dentro del ejecutable, este se vuelve más pesado.



## 16. Bibliotecas. Busca información y explica las ventajas y desventajas de usar bibliotecas dinámicas.

Ahorra más memoria, el archivo so es independiente del archivo EXE, es adecuado para el desarrollo de software a gran escala, lo que hace que el proceso sea independiente y menos acoplado.

El archivo ejecutable generado es de gran tamaño y contiene el mismo código común.

## 17. Build. Automatiza el proceso de compilación de ejecutable y biblioteca, su enlazado y la generación del archivo ejecutable para código fuente en C con make. Haz uso de un buildfile.

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej17.1.png)

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej17.2.png)

## 19. Build. Automatiza el proceso de compilación de ejecutable y biblioteca, su enlazado y la generación del archivo .jar para código fuente en Java con Maven. Haz uso de un buildfile.

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej19.1.png)

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej19.2.png)

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej19.3.png)

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej19.4.png)



## 20. Build. Automatiza el proceso de compilación de ejecutable y biblioteca, su enlazado y la generación del archivo .jar para código fuente en Java con Gradle. Haz uso de un buildfile.

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej20.png)

![Cat](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ej20.1.png)
