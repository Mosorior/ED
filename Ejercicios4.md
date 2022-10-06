# EJERCICIOS 4

## 1. Ejecuta el programa "Hola mundo" en los siguientes lenguajes:
### bash
    #!/bin/bash

    echo "Hello World"

    exit 0


### python

    print("Hello World")

### php

    <?php
    echo "Hello World";
    ?>

### javascript

    <script>
        alert('Hello World');
    </script>

### c

    #include <stdio.h>
    int main(){
        printf("Hello World");
        return 0;
    }

### c++

    #include <iostream>
    int main(){
        cout<<"Hello World";
        return 0;
    }

### java

    class HelloWorld {
        public static void main(string[] args){
            System.out.println("Hello World");
        }
    }

### ruby

File: hello_world.ruby
    puts "Hello World"

### go

    package main

    import "fmt"
    func main(){
        fmt.println("Hello World")
    }

Terminal

    $ go run hello-world.go

    $ go build hello-world.go
    $ ls

    $ ./hello-world

### rust

    fn main(){
        println!("Hello World);
    }

### lisp

    (format t "Hello, World!")

### ensamblador (nasm)

Código fuente:

    ; Define variables in the data section
SECTION .DATA
	hello:     db 'Hello world!',10
	helloLen:  equ $-hello

; Code goes in the text section
SECTION .TEXT
	GLOBAL _start 

_start:
	mov eax,4            ; 'write' system call = 4
	mov ebx,1            ; file descriptor 1 = STDOUT
	mov ecx,hello        ; string to write
	mov edx,helloLen     ; length of string to write
	int 80h              ; call the kernel

	; Terminate program
	mov eax,1            ; 'exit' system call
	mov ebx,0            ; exit with error code 0
	int 80h              ; call the kernel

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

## 4. 