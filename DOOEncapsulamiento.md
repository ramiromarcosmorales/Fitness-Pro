# Encapsulamiento
Consiste en ocultar la implementación interna de un objeto y exponerlo mediante interfaces públicas. Esto permite que los objetos mantengan su estado interno protegido de accesos no autorizados, promoviendo así la modularidad y seguridad del sistema.

# Ejemplo en el Proyecto
Se aplica el encapsulamiento en todas las clases mediante el uso de atributos privados y getters/setters para mnaipular dichos valores de los atributos.

- [Diagrama UML](https://drive.google.com/file/d/1IS_39AykBr312jyXRHkYRvfO6NLZuoFT/view)

**Justificación técnica**: La utilización de este principio, permite proteger a los objetos de accesos no autorizados, dando lugar a un sistema seguro y regulado.

# Ejemplo de Código
El siguiente código representa una clase con atributos privados y métodos getters/setters públicos, cumpliendo con las características de la herencia.
```
public class Perro {
    private int id;
    private String nombre;
    private Calendar fechaNac;
    private Propietario propietario;

    public Perro(int id, String nombre, Calendar fechaNac, Propietario propietario) {
        this.id = id;
        this.nombre = nombre;
        this.fechaNac = fechaNac;
        this.propietario = propietario;
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

    public Calendar getFechaNac() {
        return fechaNac;
    }

    public void setFechaNac(Calendar fechaNac) {
        this.fechaNac = fechaNac;
    }

    public Propietario getPropietario() {
        return propietario;
    }

    public void setPropietario(Propietario propietario) {
        this.propietario = propietario;
    }
}
```
