## Definición de Métodos

Los métodos en Ruby son definidos para realizar una tarea específica. Pueden recibir parámetros, trabajar con datos y devolver un resultado. La definición de un método en Ruby comienza con la palabra clave `def` seguida del nombre del método y opcionalmente argumentos. Termina con `end`.

### Argumentos

Los métodos pueden tomar argumentos, que son valores que pasas al método para que trabaje con ellos. Los argumentos hacen que los métodos sean más flexibles y reutilizables.

```ruby
def saluda(nombre)
  puts "Hola, #{nombre}!"
end

saluda("Nis")  # => Hola, Nis!
```

Puedes definir métodos con un número variable de argumentos usando el operador splat (`*`), o argumentos con valores por defecto, lo que los hace opcionales.

### Uso del Operador Splat (`*`) en Métodos

El operador splat (`*`) se utiliza para indicar que un método puede recibir un número variable de argumentos. Estos argumentos son agrupados en un arreglo dentro del método, permitiéndote trabajar con ellos como con cualquier otro arreglo.

Aquí tienes un ejemplo de cómo utilizar el operador splat en la definición de un método:

```ruby
def lista_de_compras(*items)
  puts "Tu lista de compras contiene #{items.length} ítems."
  items.each { |item| puts "- #{item}" }
end

lista_de_compras("Pan", "Leche", "Huevos")
```

En este ejemplo, `lista_de_compras` puede recibir cualquier número de argumentos (en este caso, ítems de la lista de compras), y los maneja dentro del método como un arreglo llamado `items`.

### Combinando Argumentos con Valores por Defecto y Splat

Además, puedes combinar argumentos con valores por defecto y el operador splat en un mismo método para lograr una mayor flexibilidad:

```ruby
def informacion_persona(nombre, edad = 30, *hobbies)
  puts "Nombre: #{nombre}, Edad: #{edad}"
  unless hobbies.empty?
    puts "Hobbies:"
    hobbies.each { |hobby| puts "- #{hobby}" }
  end
end

informacion_persona("Nis", 25, "Programar", "Leer", "Escalada")
```

En este ejemplo, `nombre` es un argumento obligatorio, `edad` tiene un valor por defecto (por lo que es opcional), y `*hobbies` captura cualquier número adicional de argumentos como un arreglo de hobbies.


```ruby
def describe_persona(nombre, edad = 18)
  puts "#{nombre} tiene #{edad} años."
end

describe_persona("Nis")  # => Nis tiene 18 años.
describe_persona("Nis", 25)  # => Nis tiene 25 años.
```

### Valores de Retorno

En Ruby, el último valor evaluado en un método es automáticamente devuelto como el valor de retorno del método. Sin embargo, puedes utilizar la palabra clave `return` para devolver un valor específico en cualquier punto del método.

```ruby
def suma(a, b)
  return a + b
end

resultado = suma(5, 3)  # => 8
```

Es importante notar que `return` termina inmediatamente la ejecución del método, por lo que cualquier código después de `return` no se ejecutará.

---

Definir y utilizar métodos es esencial para escribir código Ruby limpio y mantenible. Los métodos no solo ayudan a organizar tu código en bloques lógicos, sino que también facilitan la reutilización de código y hacen tus programas más legibles y fáciles de debuggear.
