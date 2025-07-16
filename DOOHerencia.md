# Herencia
Es un proceso fundamental que permite que una clase herede propiedades y comportamientos de otro objeto. Esto fomenta la reutilización del código y la creación de jerarquías de clases, donde las clases secundarias pueden extender o modificar el comportamiento de las clases primarias.

# Ejemplo en el Proyecto 

Si bien el proyecto original no implementó herencia, se realizo un nuevo analisís y se decidió realizar la siguiente mejora: la clase Membresía pasa a ser abstracta, contiene los atributos y métodos básicos, y luego se crean sub-clases para representar los tipos de membresías.
- [Diagrama UML](https://drive.google.com/file/d/1K_jN4m9WBeuxVqOSuiEBKBCtUU5M1NFK/view?usp=sharing)

**Justificación técnica**: La utilización de este principio permitió la reutilización del código y tener un punto de vista jerarquico de las clases.

# Ejemplo en el Código
El siguiente código es una clara representación de como podemos aplicar la herencia: la clase Membresía define atributos y comportamientos que toda clase hija va a compartir. Por otro lado, la clase Membresía Basica hereda de Membresia y implementa su propia lógica, y de ser necesario puede definir atributos o métodos adicionales.

## Clase Membresía
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

    public Boolean consultarEstado() {
        return fechaVenc.after(Calendar.getInstance());
    }

    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public ETipos getTipo() {
        return tipo;
    }

    public void setTipo(ETipos tipo) {
        this.tipo = tipo;
    }

    public Calendar getFechaVenc() {
        return fechaVenc;
    }

    public void setFechaVenc(Calendar fechaVenc) {
        this.fechaVenc = fechaVenc;
    }

    public int getLimite() {
        return limite;
    }

    public void setLimite(int limite) {
        this.limite = limite;
    }
}
```

## Clase Membresía Basica
```
public class MembresiaBasica extends Membresia {

    public MembresiaBasica(int id, Calendar fechaVenc) {
        super(id, ETipos.BASICA, fechaVenc, 20);
    }

    @Override
    public void reservarClase() {
        System.out.println("Podes reservar hasta " + getLimite() + " clases.");
    }
}
```
