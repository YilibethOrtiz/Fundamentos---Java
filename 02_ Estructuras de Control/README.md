## 📘 Módulo 2: Estructuras Condicionales (`if`, `else if`, `else`)

Las estructuras condicionales permiten que el programa tome decisiones y ejecute diferentes bloques de código dependiendo de si una condición lógica se cumple (`true`) o no (`false`).

---

### 1. Condicional Simple (`if`)
Se utiliza cuando solo te interesa ejecutar un bloque de código si una condición específica es verdadera. Si es falsa, el programa simplemente continúa su camino.

> **"Si pasa esto, hago aquello. Si no pasa, sigo de largo y no hago nada."**

*   **En la vida real:** "Si el temporizador de la lavadora suena, voy a sacar la ropa." (Si no suena, sigo haciendo lo mío en la computadora).
*   **En la universidad:** "Si el profesor sube la nota de la defensa del proyecto, entro a revisarla."

*   **Sintaxis:**
    ```java
    if (condicion) {
        // Código que se ejecuta si es verdadero
    }
    ```
*   **Ejemplo Mínimo:**
    ```java
    int edad = 20;
    if (edad >= 18) {
        System.out.println("Es mayor de edad.");
    }
    ```

---

### 2. Condicional Compuesta (`if - else`)
Se utiliza cuando tienes dos caminos posibles: uno si la condición se cumple y otro completamente diferente si no se cumple.
> **"Tengo dos caminos obligatorios. Si se cumple la condición, hago la opción A; si no se cumple, hago la opción B sí o sí."**

*   **En la logística de envíos:** "Si el cliente pagó el delivery rápido, le envío el paquete hoy mismo por motorizado. De lo contrario, se lo mando mañana en el despacho normal."
*   **En el hogar:** "Si los niños terminaron la tarea, los dejo ver un rato televisión. De lo contrario, se me van a dormir ya."
*   **En el software:** "Si el usuario pone la contraseña correcta, entra al sistema. De lo contrario, le muestro un cartel rojo de error."

*   **Sintaxis:**
    ```java
    if (condicion) {
        // Código si es verdadero
    } else {
        // Código si es falso
    }
    ```
*   **Ejemplo Mínimo:**
    ```java
    boolean tieneAcceso = false;
    if (tieneAcceso) {
        System.out.println("Bienvenido.");
    } else {
        System.out.println("Bloqueado.");
    }
    ```

---

### 3. Condicional Múltiple (`if - else if - else`)
Se utiliza cuando necesitas evaluar tres o más alternativas distintas en cadena. En el momento en que una condición se cumpla, Java ejecuta ese bloque y descarta el resto.

> **"Tengo varias opciones en fila. Voy revisando una por una de arriba a abajo. En la primera que funcione me quedo, y si ninguna sirve, aplico el plan por defecto."**

*   **Organizando el día:** "Si los niños están despiertos, les preparo la cena. Si no, pero tengo reunión del proyecto con mi equipo, me conecto a la llamada. Y si no hay nada de eso pendiente, me pongo a adelantar mi reto de código."
*   **Clasificando el inventario:** "Si tengo más de 20 franelas en el estante, el stock está perfecto. Si tengo entre 1 y 5, tengo que reponer inventario rápido. De lo contrario (si está en 0), pongo el aviso de 'Agotado' en la página."

*   **Sintaxis:**
    ```java
    if (condicion1) {
        // Código si condicion1 es verdadera
    } else if (condicion2) {
        // Código si condicion1 fue falsa pero condicion2 es verdadera
    } else {
        // Código por defecto si ninguna de las anteriores se cumplió
    }
    ```
*   **Ejemplo Mínimo:**
    ```java
    int calificacion = 8;
    if (calificacion >= 9) {
        System.out.println("Excelente");
    } else if (calificacion >= 5) {
        System.out.println("Aprobado");
    } else {
        System.out.println("Reprobado");
    }
    ```
---
### 4. Condicionales Anidados (`if` dentro de otro `if`)
> **"Para tomar una decisión, primero tengo que haber pasado por un filtro anterior. Es una condición dentro de otra."**

*   **En la logística de mi negocio:** "Primero verifico si hay telas en existencia. **SI HAY**, entonces paso a revisar el segundo filtro: si la máquina de bordar está libre, empiezo a fabricar; si la máquina está ocupada, la prenda queda en espera. **SI NO HABÍA** telas desde el principio, ni siquiera reviso la máquina, directo le digo al cliente que no se puede hacer."
*   **En el hogar:** "Primero reviso si los niños terminaron la cena. **SI SÍ**, paso al segundo filtro: si ya ordenaron sus juguetes, los dejo ver televisión; si no han ordenado, se ponen a recoger. **SI NO** terminaron la cena desde el principio, no hay televisión ni juegos, se quedan en la mesa."

*   **Ejemplo**
```java
public class ProduccionTextil {
    public static void main(String[] args) {
        boolean hayTelas = true;
        boolean maquinaLibre = false;
        
        System.out.println("--- CONTROL DE PRODUCCIÓN ---");
        
        if (hayTelas) {
            if (maquinaLibre) {
                System.out.println("Resultado: Fabricando prenda.");
            } else {
                System.out.println("Resultado: En espera (Máquina ocupada).");
            }
        } else {
            System.out.println("Resultado: Cancelado (Sin telas).");
        }
    }
}
```   
    
