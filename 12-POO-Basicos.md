## Conceptos Básicos de OOP

La Programación Orientada a Objetos (OOP) es un paradigma de programación que utiliza objetos y clases para organizar el código. Es especialmente poderosa para modelar sistemas complejos y facilitar el mantenimiento y la escalabilidad del software.

### Clases

Una clase en Ruby es como un molde que define las propiedades (atributos) y comportamientos (métodos) comunes de un objeto. Las clases se utilizan para crear instancias de objetos.

```ruby
class Persona
  def initialize(nombre)
    @nombre = nombre  # @nombre es una variable de instancia
  end

  def saluda
    "Hola, mi nombre es #{@nombre}"
  end
end
```

### Objetos

Un objeto es una instancia de una clase. Cada objeto tiene su propio conjunto de datos y comportamientos, definidos por su clase. Puedes crear un objeto llamando al método `.new` de una clase.

```ruby
persona = Persona.new("Nis")
puts persona.saluda  # => "Hola, mi nombre es Nis"
```

### Métodos de Instancia y de Clase

- **Métodos de Instancia**: Son métodos que se llaman en instancias de una clase. Utilizan los datos específicos de la instancia para realizar operaciones. En el ejemplo anterior, `saluda` es un método de instancia.

- **Métodos de Clase**: Son métodos que se llaman en la clase misma, no en instancias de la clase. Se definen anteponiendo `self.` al nombre del método o colocando el método dentro de un bloque `class << self`.

```ruby
class Persona
  def self.descripcion
    "Esta es una clase para crear personas."
  end
end

puts Persona.descripcion  # => "Esta es una clase para crear personas."
```

---

La Programación Orientada a Objetos te permite modelar entidades del mundo real de manera intuitiva, haciendo tu código más organizado, reutilizable y fácil de entender. Ruby, con su sintaxis limpia y su enfoque en la simplicidad, es un lenguaje excelente para aprender y aplicar los principios de la OOP.

Explorar estos conceptos te dará una base sólida no solo en Ruby sino en la programación en general, abriendo las puertas a patrones de diseño avanzados y mejores prácticas en el desarrollo de software.


[:arrow_backward:](11-Bloques-Procs-Lambdas.md) [:arrow_forward:](13-Atributos.md)