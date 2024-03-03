## Atributos y Accesores

En Ruby, los atributos de un objeto son simplemente las variables de instancia que almacenan los datos del objeto. Los accesores son métodos que permiten leer y escribir en estas variables de instancia desde fuera de la clase.

### attr_reader

`attr_reader` genera automáticamente métodos de solo lectura para las variables de instancia especificadas. Esto significa que podrás obtener el valor de estas variables, pero no modificarlas directamente.

```ruby
class Persona
  attr_reader :nombre

  def initialize(nombre)
    @nombre = nombre
  end
end

persona = Persona.new("Nis")
puts persona.nombre  # => Nis
# persona.nombre = "Otro Nombre"  # Esto lanzaría un error
```

### attr_writer

`attr_writer` hace lo contrario a `attr_reader`; genera automáticamente métodos de solo escritura para las variables de instancia especificadas. Podrás cambiar el valor de estas variables, pero no leerlas directamente.

```ruby
class Persona
  attr_writer :nombre

  def initialize(nombre)
    @nombre = nombre
  end
end

persona = Persona.new("Nis")
persona.nombre = "Otro Nombre"  # Esto es posible
# puts persona.nombre  # Esto lanzaría un error
```

### attr_accessor

`attr_accessor` es la combinación de `attr_reader` y `attr_writer`, generando métodos tanto de lectura como de escritura para las variables de instancia especificadas. Esto te permite tanto leer como modificar los valores de estas variables.

```ruby
class Persona
  attr_accessor :nombre

  def initialize(nombre)
    @nombre = nombre
  end
end

persona = Persona.new("Nis")
puts persona.nombre  # => Nis
persona.nombre = "Otro Nombre"
puts persona.nombre  # => Otro Nombre
```

---

El uso de `attr_reader`, `attr_writer`, y `attr_accessor` facilita la gestión de los atributos de tus objetos, haciendo tu código más limpio y fácil de mantener. Al definir claramente cómo se pueden acceder y modificar los datos de un objeto, también mejoras la seguridad y la integridad de tus programas.

[:arrow_backward:](11-Bloques-Procs-Lambdas.md) [:arrow_forward:](14-Herencia.md)

