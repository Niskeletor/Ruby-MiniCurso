## Módulos y Mixins

### Namespacing

El namespacing es una técnica que utiliza módulos para agrupar clases, métodos u otros módulos relacionados bajo un mismo contexto o nombre de módulo. Esto ayuda a evitar conflictos de nombres en programas grandes donde es posible que diferentes partes quieran usar el mismo nombre para diferentes clases o métodos.

```ruby
module Transporte
  class Coche
    def arrancar
      puts "El coche está arrancando"
    end
  end
end

mi_coche = Transporte::Coche.new
mi_coche.arrancar  # => "El coche está arrancando"
```

Aquí, `Transporte` es un módulo que actúa como un namespace para la clase `Coche`. Esto significa que puedes tener otra clase `Coche` fuera del módulo `Transporte` sin causar conflictos de nombres.

### Mixins

Los mixins permiten incluir módulos en clases para proporcionarles métodos adicionales, lo que es una forma poderosa de agregar funcionalidades a clases sin heredar de una superclase. Ruby utiliza los métodos `include` y `prepend` para mezclar un módulo en una clase, y `extend` para agregar los métodos de un módulo como métodos de clase.

```ruby
module Arrancable
  def arrancar
    puts "El vehículo está arrancando"
  end
end

class Coche
  include Arrancable
  # prepend Arrancable se usaría si quisiéramos que los métodos del módulo
  # sobreescriban los métodos de la clase en caso de conflicto.
end

mi_coche = Coche.new
mi_coche.arrancar  # => "El vehículo está arrancando"
```

Usando mixins, puedes diseñar tus módulos para ser reutilizados en varias clases. Esto promueve el principio DRY (Don't Repeat Yourself - No te repitas) y facilita la mantenibilidad del código.

---

Los módulos y mixins son herramientas esenciales en Ruby que te ofrecen flexibilidad para organizar y reutilizar tu código de manera efectiva. Entender cómo y cuándo usarlos te permitirá construir aplicaciones Ruby más modulares, limpias y eficientes.

 [:arrow_backward:](14-Herencia.md) [:arrow_forward:](16-Datos-Avanzados.md)