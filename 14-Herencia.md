## Herencia

La herencia permite que una clase (subclase) herede el comportamiento (métodos) y los atributos de otra clase (superclase). Esto facilita la especialización de clases sin tener que reescribir código.

### Superclase y Subclase

En Ruby, se utiliza el símbolo `<` para denotar herencia. La clase a la derecha del `<` es la superclase, y la clase a la izquierda es la subclase.

```ruby
class Vehiculo
  def arrancar
    puts 'El vehículo está arrancando'
  end
end

class Coche < Vehiculo
  def encender_radio
    puts 'La radio se está encendiendo'
  end
end

coche = Coche.new
coche.arrancar       # => El vehículo está arrancando
coche.encender_radio # => La radio se está encendiendo
```

En este ejemplo, `Coche` hereda de `Vehiculo`, lo que significa que `Coche` es un tipo de `Vehiculo` y puede usar sus métodos, como `arrancar`, además de sus propios métodos, como `encender_radio`.

### Método super

El método `super` se utiliza dentro de los métodos de la subclase para llamar a la versión del mismo método definido en la superclase. Esto es útil cuando se desea ampliar la funcionalidad de un método heredado, en lugar de reemplazarlo completamente.

```ruby
class Vehiculo
  def arrancar
    puts 'El vehículo está arrancando'
  end
end

class Coche < Vehiculo
  def arrancar
    super
    encender_radio
  end

  def encender_radio
    puts 'La radio se está encendiendo'
  end
end

coche = Coche.new
coche.arrancar
# => El vehículo está arrancando
# => La radio se está encendiendo
```

En este caso, `Coche#arrancar` extiende la funcionalidad del método `arrancar` de la `Vehiculo` llamando primero al método de la superclase con `super` y luego ejecutando su propia lógica adicional.

---

La herencia y el uso adecuado del método `super` son fundamentales para aprovechar la potencia de la programación orientada a objetos en Ruby, permitiéndote crear aplicaciones más modulares, reutilizables y fáciles de mantener.
