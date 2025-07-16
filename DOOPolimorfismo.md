# Polimorfismo
Consiste en la capacidad de los objetos de una misma jerarquía de clases para responder de una manera diferente a un mismo mensaje. El uso del polimorfismo promueve un código más flexible, reutilizable y extensible.

# Ejemplo en el Proyecto
En el siguiente diagrama se aplica en la clase padre Membresía, donde posee un metodo abstracto llamado reservarClase(). Las clases hijas implementaran este método con su lógica correspondiente.

- [Diagrama UML](https://drive.google.com/file/d/1K_jN4m9WBeuxVqOSuiEBKBCtUU5M1NFK/view?usp=sharing)

**Justificación técnica**: Cada clase implementa la lógica del método reservarClase() a su manera, esto permite que se pueda invocar al método desde un objeto Membresía sin importar su implementación concreta. 

# Ejemplo de Código
El siguiente código contiene un metodo abstracto 
```
public abstract class Membresia {
    private int id;
    private ETipos tipo;
    private Calendar fechaVenc;
    private int limite;

    public Membresia(int id, ETipos tipo, Calendar fechaVenc, int limite) {
        this.id = id;
        this.tipo = tipo;
        this.fechaVenc = fechaVenc;
        this.limite = limite;
    }

    public abstract void reservarClase();
}
```  
