---

### 5. Toma de decisiones múltiples con `switch`
> **"Tengo un caso específico y busco directamente en una lista de opciones a ver con cuál combina. Es como ir directo al grano sin tener que evaluar un 'si no' cada vez."**

* **En la logística de mi negocio (Menú de envíos):** "Reviso qué empresa eligió el cliente. Si eligió **'MRW'**, calculo el precio para esa agencia; si eligió **'Zoom'**, aplico su tarifa; si eligió **'Tealca'**, uso la de ellos. Si no eligió ninguna de la lista, uso el envío por defecto de la casa."
* **En el hogar (Días de la semana):** "Miro qué día es hoy. Si es **'Lunes'**, toca organizar la casa; si es **'Sábado'**, es día de paseo con los niños; si es **'Domingo'**, es día de descanso. Para cualquier otro día, la rutina es normal de estudio y trabajo."

#### 💻 Ejemplo de código básico en Java:
```java
public class ControlEnvios {
    public static void main(String[] args) {
        String agencia = "Zoom"; // Cambia por "MRW" o "Tealca"
        
        System.out.println("--- CONTROL DE ENVÍOS (SWITCH) ---");
        
        switch (agencia) {
            case "MRW":
                System.out.println("Resultado: Despachar por MRW.");
                break;
            case "Zoom":
                System.out.println("Resultado: Despachar por Zoom.");
                break;
            case "Tealca":
                System.out.println("Resultado: Despachar por Tealca.");
                break;
            default:
                System.out.println("Resultado: Agencia no registrada. Usar despacho local.");
                break;
        }
    }
}
