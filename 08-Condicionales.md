## Condicionales

En Ruby, los condicionales te permiten tomar decisiones en tu código basadas en si una o más condiciones son verdaderas o falsas. Esto es esencial para ejecutar diferentes bloques de código según distintos escenarios. Aquí exploraremos las estructuras condicionales más comunes: `if`, `else`, `elsif`, `unless`, y `case`.

### if, else, elsif

La estructura `if` te permite ejecutar un bloque de código si una condición es verdadera. Puedes complementarla con `else` para ejecutar un bloque diferente si la condición es falsa, y con `elsif` para verificar condiciones adicionales si las anteriores son falsas.

```ruby
edad = 20

if edad >= 18
  puts "Eres mayor de edad."
elsif edad < 18 && edad > 0
  puts "Eres menor de edad."
else
  puts "Edad no válida."
end
```

### unless

`unless` es un condicional que hace lo opuesto a `if`: se ejecuta cuando la condición es falsa. Es útil para mejorar la legibilidad del código cuando quieres verificar la negación de una condición.

```ruby
llueve = false

unless llueve
  puts "Hace un buen día para salir."
else
  puts "Hace un buen día para mojarse."
end
```

### case

El condicional `case` permite comparar una variable con una serie de valores, ejecutando el primer bloque de código cuyo valor coincida. Es una alternativa a una serie de `if...elsif` y es particularmente útil cuando se trabaja con múltiples condiciones que dependen del mismo valor.

```ruby
dia = "Lunes"

case dia
when "Lunes"
  puts "Inicio de la semana laboral."
when "Viernes"
  puts "Casi es fin de semana!."
else
  puts "Un día más de trabajo."
end
```

---

Los condicionales son herramientas poderosas que te permiten escribir programas que pueden tomar decisiones y comportarse de manera diferente bajo distintas circunstancias. Experimentar con estas estructuras te ayudará a entender mejor cómo y cuándo utilizarlas para controlar el flujo de tus programas en Ruby.

[:arrow_backward:](07-Operadores.md) [:arrow_forward:](09-Bucles.md)