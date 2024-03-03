## Bloques, Procs y Lambdas

Ruby proporciona varias formas de manejar bloques de código que pueden ser pasados a métodos y ejecutados. Vamos a explorar cómo funcionan los bloques, los objetos `Proc` y las expresiones `lambda`.

### Bloques

Un bloque es una porción de código que puede ser pasada a un método para ser ejecutada. Los bloques pueden definirse con las llaves `{}` para bloques de una sola línea o con `do...end` para bloques de múltiples líneas.

#### Uso de `yield`

Dentro de un método, puedes usar `yield` para llamar al bloque que fue pasado al método.

```ruby
def ejecuta_bloque
  yield if block_given?
end

ejecuta_bloque { puts "Hola desde el bloque!" }
```

`block_given?` es un método que verifica si se ha pasado un bloque al método actual.

### Proc

Un `Proc` (procedimiento) es un bloque de código que ha sido encapsulado en un objeto. Esto te permite almacenar bloques de código en variables, pasarlos como argumentos a métodos y ejecutarlos más tarde.

```ruby
saludo = Proc.new { |nombre| puts "Hola, #{nombre}!" }
saludo.call("Nis")
```

### Lambda

Una `lambda` es similar a un `Proc`, pero con algunas diferencias en cuanto a cómo maneja los argumentos y cómo retorna valores desde dentro del bloque.

```ruby
saludo_lambda = lambda { |nombre| puts "Hola, #{nombre}!" }
saludo_lambda.call("Nis")
```

#### Diferencias entre Procs y Lambdas

1. **Argumentos**: Una lambda verifica la cantidad de argumentos pasados a ella y lanzará un error si no coinciden. Un `Proc` ignora argumentos extra y asigna `nil` a cualquier argumento faltante.
2. **Retorno**: Al retornar dentro de una lambda, solo se sale de la lambda. Al retornar dentro de un Proc, se sale del método que contiene al Proc.

---

Los bloques, Procs y Lambdas son herramientas increíblemente poderosas en Ruby, ofreciendo una gran flexibilidad para manejar código que se ejecuta dentro de tus métodos. Aprender a utilizarlos efectivamente abrirá nuevas puertas para escribir código más limpio, modular y reutilizable.
