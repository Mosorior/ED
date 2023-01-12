# Tema 7 - Optimización (Ejercicios)

## 1. ¿Qué se entiende por hediondez del código?

Es un código que a pesar de no funcionar mal, puede provocar errores en un futuro además de realentizar el programa.

## 2. ¿Qué tipo de herramienta utilizamos para hacer análisis estático del código?

Se usan linters.

## 3. ¿Qué sitios web nos permiten hacer análisis estático del código o **Continuous Inspection**?

Scrutinizer o SonarQube.

## 4. Instala en IntelliJ el plugin **Spot**Bugs, si no lo tienes aún instalado.

![No se usa ya](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ejercicios7/Ej04

.png)

## 5. Realiza **análisis estático de código** para las clases del proyecto *miapp*. Consulta el siguiente enlace: [análisis estático con SpotBugs](https://github.com/jamj2000/DAW1-ED-Pruebas-Ejemplo1#análisis-estático-de-código-con-findbugs-en-netbeans).

![No se usa ya](https://raw.githubusercontent.com/Mosorior/ED/main/images/Ejercicios7/Ej05.png)

## 6. Indica al menos un `code smell` relevante de cada clase. Explica cómo podría solucionarse.

Long Method (Bloater): Se puede usar el refactor Extract Method. Si interfieren parámetros y variables locales, podemos emplear otros refactors para usar objetos de parámetros y reemplazar variables temporales con métodos.

Refused bequest (Object-Orientation Abusers): Si la herencia no tiene sentido alguno, se debe reemplazar con delegación al objeto. Si tiene sentido, hay que extraer una superclase para obtener las variables y el comportamiento que necesitemos. Bequest se refiere a que la subclase rechaza el comportamiento de la clase padre que no necesita.

Shotgun Surgery (Change Preventers): Mover todo el comportamiento similar a una clase sola, así cada una tendrá su propia responsabilidad. Recordar el principio de *single responsibility*. Si no existe una clase apropiada a donde mover el comportamiento, crearla.

## 7. ¿Qué es la refactorización?

Es el proceso de reestructurar un código fuente, alterando su estructura interna sin cambiar su comportamiento externo.

## 8. ¿Qué técnicas se utilizan a menudo a la hora de refactorizar?

- Renombrado de variables
- Pasar código duplicado a funciones
- Eliminación de código inalcanzable
- Eliminación de código redundante
- Eliminación de código muerto
