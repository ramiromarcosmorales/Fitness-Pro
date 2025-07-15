# Abstracción
Consiste en la simplificación de la complejidad del mundo real, modelando solo los aspectos esenciales y relevantes para el sistema. Esto permite un diseño de sistema mas claro, reutilizable y mantenible.
La aplicación de este principio nos ayuda a poner foco en lo qué hace el objeto, en lugar de cómo lo hace, promoviendo la separabilidad de responsabilidades.

# Ejemplo en el Proyecto
Se aplica la abstracción al momento de modelar las entidades como "Empleado", "Socio" y "Maquina", solo se detallan sus características y comportamientos necesarios para el funcionamiento.

// [Diagrama de Clases](https://drive.google.com/file/d/1IS_39AykBr312jyXRHkYRvfO6NLZuoFT/view) 

**Justificación técnica**: La utilización de este principio, permite representar únicamente las características y funcionalidades para el sistema, evitando agregando información innecesaria.


# Ejemplo de Código
El siguiente código representa una clase Abstracta donde solo se definen las características y comportamientos principales de Persona.
```
public abstract class Persona {
    private int id;
    private String nombre;
    private String apellido;
    private Calendar fechaNacimiento;

    public Persona(int id, String nombre, String apellido, Calendar fechaNacimiento) {
        this.id = id;
        this.nombre = nombre;
        this.apellido = apellido;
        this.fechaNacimiento = fechaNacimiento;
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getNombre() {
        return nombre;
    }

    public void setNombre(String nombre) {
        this.nombre = nombre;
    }

    public String getApellido() {
        return apellido;
    }

    public void setApellido(String apellido) {
        this.apellido = apellido;
    }

    public Calendar getFechaNacimiento() {
        return fechaNacimiento;
    }

    public void setFechaNacimiento(Calendar fechaNacimiento) {
        this.fechaNacimiento = fechaNacimiento;
    }
}
```
