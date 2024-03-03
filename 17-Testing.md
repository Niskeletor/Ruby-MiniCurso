## Testing en Ruby

### Introducción al Testing

El testing (pruebas) en Ruby se puede realizar de varias maneras, pero los dos enfoques más comunes son mediante el uso de la librería estándar `Test::Unit` y la gema `RSpec`. Realizar pruebas te permite verificar que tu código hace lo que esperas que haga y es fundamental para el desarrollo de software ágil y confiable.

### Test Unit

`Test::Unit` es un framework de testing que viene incluido con Ruby. Permite escribir pruebas unitarias que verifican la funcionalidad de una pequeña parte del código. Con `Test::Unit`, defines clases de prueba que heredan de `Test::Unit::TestCase` y escribes métodos de prueba dentro de ellas.

```ruby
require 'test/unit'

class MiTest < Test::Unit::TestCase
  def test_que_algo_es_verdadero
    assert true
  end
end
```

Cada método de prueba debe comenzar con `test_` y puedes usar aserciones para verificar que tu código se comporta como esperas.

### RSpec

`RSpec` es una gema de Ruby que proporciona un lenguaje de dominio específico (DSL) para escribir pruebas. Es muy popular en la comunidad Ruby por su sintaxis expresiva y legible. Para usar RSpec, necesitas agregarlo a tu proyecto e instalarlo.

```ruby
# Gemfile
gem 'rspec'
```

Luego, puedes escribir especificaciones de RSpec que describan el comportamiento esperado de tu código:

```ruby
require 'rspec'

describe 'Una descripción de lo que estás probando' do
  it 'hace algo esperado' do
    expect(algo).to eq(algo_esperado)
  end
end
```

RSpec anima a escribir tus pruebas en un estilo muy legible, casi como si estuvieras describiendo el comportamiento esperado en inglés.

---

El testing es una parte integral del desarrollo y adoptar buenas prácticas de testing desde el principio de tu proyecto puede ahorrarte muchos dolores de cabeza más adelante. Tanto `Test::Unit` como `RSpec` ofrecen herramientas poderosas para ayudarte a escribir pruebas efectivas para tu código Ruby.

 [:arrow_backward:](16-Datos-Avanzados.md) [:arrow_forward:](18-Intro-Ruby-on-Rails.md)
 