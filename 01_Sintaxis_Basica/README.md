# 📁 Módulo 1: Sintaxis Básica y Variables en Java

En este módulo se abordan los componentes elementales de un programa en Java. Comprender cómo la computadora almacena la información en la memoria y cómo estructurar las primeras líneas de código es crucial para desarrollar una lógica de programación sólida.

---

## 📘 1. Fundamentos Teóricos

### El Método Principal: `public static void main(String[] args)`
En Java, toda aplicación ejecutable debe contener obligatoriamente este método. Es conocido como el **punto de entrada** (*entry point*). Cuando ordenas a la computadora ejecutar tu programa, la Máquina Virtual de Java (JVM) busca exactamente esta línea para saber por dónde empezar a leer el código.

###Ejemplo 

public class EstructuraMinima {
    public static void main(String[] args) {
        // Aquí adentro va todo el código que quieres que se ejecute
        System.out.println("¡Punto de entrada activado!");
    }
}

---
### ¿Qué es una Variable?
Desde una perspectiva técnica, una **variable** es un espacio reservado en la memoria RAM de la computadora al que se le asigna un nombre (identificador) y un tipo de dato específico. Sirve para almacenar datos temporalmente durante la ejecución del programa.

En Java, el tipado es **estático y fuerte**, lo que significa que debes declarar obligatoriamente el tipo de dato que va a guardar la variable antes de usarla, y ese tipo no puede cambiar después.

### Tipos de Datos Primitivos Comunes
Los tipos primitivos son aquellos que vienen integrados directamente en el lenguaje y almacenan valores puros (no son objetos):

*   **`int` (Entero):** Almacena números enteros sin decimales (ej. `23`, `-5`, `100`). Utiliza 32 bits de memoria.
###Ejemplo de int (Entero):
public class EjemploEntero {
    public static void main(String[] args) {
        int cantidadEstudiantes = 45;
        int añoActual = 2026;
        
        System.out.println("Estudiantes en el salón: " + cantidadEstudiantes);
        System.out.println("Año del curso: " + añoActual);
    }
}
---   
*   **`double` (Decimal de doble precisión):** Se usa para números con punto decimal (ej. `19.5`, `3.1416`). Es el estándar para cálculos precisos.
### Ejemplo de double (Decimales):

public class EjemploDecimal {
    public static void main(String[] args) {
        double notaExamen = 19.5;
        double temperaturaMaracaibo = 34.8;
        
        System.out.println("Tu nota es: " + notaExamen);
        System.out.println("Temperatura actual: " + temperaturaMaracaibo + "°C");
    }
}

---
*   **`boolean` (Booleano):** Solo puede almacenar uno de dos valores posibles: `true` (verdadero) o `false` (falso). Es la base de la lógica condicional.
##Ejemplo de boolean:

public class EjemploBooleano {
    public static void main(String[] args) {
        boolean claseFinalizada = false;
        boolean tieneInscripcion = true;
        
        System.out.println("¿Terminó la clase?: " + claseFinalizada);
        System.out.println("¿Está inscrito?: " + tieneInscripcion);
    }
}

---

*   **`char` (Carácter):** Almacena un único carácter o símbolo utilizando comillas simples (ej. `'A'`, `'7'`, `'#'`).
##Ejemplo de char:

public class EjemploCaracter {
    public static void main(String[] args) {
        char seccionUniversidad = 'A';
        char inicialNombre = 'Y';
        
        System.out.println("Te toca en la sección: " + seccionUniversidad);
        System.out.println("La inicial de tu nombre es: " + inicialNombre);
    }
}

---  

> ⚠️ **Nota importante sobre `String`:** A diferencia de los anteriores, `String` (Cadena de texto) **no es un tipo primitivo**, sino una Clase en Java. Se utiliza para almacenar texto estructurado (ej. `"Hola Mundo"`) y siempre se escribe con la primera **S** en mayúscula y comillas dobles.
##Ejemplo String:

public class EjemploTexto {
    public static void main(String[] args) {
        String universidad = "Universidad Bolivariana de Venezuela";
        String carrera = "Informática para la Gestión Social";
        
        System.out.println("Estudio en la: " + universidad);
        System.out.println("Carrera: " + carrera);
    }
}

---

## 💻 2. Código Explicado Paso a Paso

A continuación se presenta el código fuente de un programa clásico. En él se declaran diferentes tipos de variables, se realizan operaciones aritméticas básicas y se muestra el resultado textualmente por consola.

```java
// Archivo: EstructuraBasica.java
package 01_Sintaxis_Basica;

public class EstructuraBasica {
    
    // El punto de entrada del programa
    public static void main(String[] args) {
        
        // 1. Declaración e inicialización de variables
        String nombreEstudiante = "Yilibeth";
        int edad = 23;
        double notaPrimerParcial = 18.5;
        double notaSegundoParcial = 16.0;
        boolean estaAprobado = true;
        
        // 2. Operación aritmética (Procesamiento de datos)
        // Calculamos el promedio sumando ambas notas y dividiendo entre dos
        double promedioFinal = (notaPrimerParcial + notaSegundoParcial) / 2.0;
        
        // 3. Salida de datos por consola
        // Usamos System.out.println para mostrar la información en la pantalla
        System.out.println("--- Reporte del Estudiante ---");
        System.out.println("Nombre: " + nombreEstudiante);
        System.out.println("Edad: " + edad + " años");
        System.out.println("Promedio Obtenido: " + promedioFinal);
        System.out.println("¿Estado aprobado?: " + estaAprobado);
    }
}
