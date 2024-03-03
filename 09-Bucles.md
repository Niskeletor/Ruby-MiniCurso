## Bucles

Los bucles permiten ejecutar un bloque de código repetidamente bajo ciertas condiciones. Ruby ofrece varias formas de crear bucles, facilitando la elección de la herramienta adecuada para cada tarea.

### while

El bucle `while` repite un bloque de código mientras una condición sea verdadera. Es útil cuando no sabes cuántas veces necesitas iterar de antemano.

```ruby
contador = 1

while contador <= 5
  puts "Iteración #{contador}"
  contador += 1
end
```

### until

`until` es el complemento de `while`: ejecuta un bloque de código hasta que una condición se vuelve verdadera, es decir, sigue iterando mientras la condición sea falsa.

```ruby
contador = 1

until contador > 5
  puts "Iteración #{contador}"
  contador += 1
end
```

### for

El bucle `for` se utiliza para iterar sobre un rango o una colección. Es una forma más sintética de realizar iteraciones, especialmente útil cuando conoces el rango de valores sobre el que quieres iterar.

```ruby
for numero in 1..5
  puts "Número #{numero}"
end
```

### .each

El método `.each` es preferido en Ruby para iterar sobre elementos de una colección, como arrays o hashes. Es más idiomático que `for` y ofrece un mejor control sobre la colección.

```ruby
[1, 2, 3, 4, 5].each do |numero|
  puts "Número #{numero}"
end
```

### .times

El método `.times` es una forma sencilla de ejecutar un bucle un número específico de veces. Es especialmente útil cuando sabes exactamente cuántas iteraciones necesitas.

```ruby
5.times do |numero|
  puts "Iteración #{numero + 1}"
end
```

---

Cada uno de estos bucles tiene su propósito y situación donde brilla más. Experimentar con ellos te ayudará a comprender mejor sus diferencias y cuándo usar cada uno. Los bucles son una parte integral de la programación en Ruby, permitiéndote automatizar tareas repetitivas de manera eficiente.
    
    [:arrow_backward:](/04-Sintaxis/README.md) [:arrow_forward:](/06-Métodos/README.md)