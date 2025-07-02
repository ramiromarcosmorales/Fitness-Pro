# Aplicación del Patrón de Diseño Singleton

# Propósito y Tipo del Patrón
El gimnasio Fitness Pro enfrenta problemas de inoperancia y errores en el registro manual de pagos de los socios. Este enfoque manual provoca: retrasos, inconsistencias y dificultades, teniendo un impacto negativo en la eficiencia y experiencia del cliente, ya que los registros no son confiables ni accesibles de forma moderna
Para abordar este problema, aplicaremos el patrón de diseño Singleton, que se utiliza para garantizar que haya una única instancia de la clase encargada del registro de pagos.

# Motivación
El sistema de registro manual de pagos genera inconvenientes para el personal como para el socio, uno de lo más comunes son: errores humanos, retrasos para verificar los pagos y dificultad de consultar los pagos.

El patrón de diseño Singleton va a permitir resolver estos problemas mediante la creación de un sistema globalizado que permita gestionar los pagos, esto incluye: automatización ,y consistencia de datos.
Al aplicar este patron de diseño el gimnasio va a tener un sistema moderno, rápido y confiable, logrando una mejor experiencia tanto para el personal como para el socio.

# Estructura de Clases

[Diagrama de Clases v3](https://drive.google.com/file/d/1b_up4em75Zsy8p8W1IDlDHV3uL1nVfaE/view?usp=sharing)

![Estructura de Clase](https://drive.google.com/uc?id=1HlqWM3ING3fgS0mYz1fE9MCu9KQ5_dq4)

# Ejemplo de Código


## Clase Pago

```
public class Pago {
    private String socio;
    private double total;

    public Pago(String socio, double total) {
        this.socio = socio;
        this.total = total;
    }

    public String gettPago() {
        return "Socio: " + socio + " Total: " + total;
    }

    public String getSocio() {
        return socio;
    }

    public double getTotal() {
        return total;
    }
}
```

## Instancia de la Clase Pago

```
public class Main {
    public static void main(String[] args) {
        Pago pago1 = new Pago("Ramiro", 1045.40);
        Pago pago2 = new Pago("Felipe", 1564.50);
        Pago pago3 = new Pago("Bautista", 4343.20);
    }
}
```
