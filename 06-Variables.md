## Variables y Asignación

En Ruby, las variables son utilizadas para almacenar datos que pueden ser utilizados y modificados por el programa. Existen diferentes tipos de variables, cada una con su propio alcance y propósito. Veamos cómo funcionan las variables locales, globales y las constantes en Ruby.

### Variables Locales

Las variables locales son quizás las más comunes en la programación Ruby. Su alcance está limitado al contexto en el que son creadas, como dentro de un método o un bloque de código. Se nombran comenzando con una letra minúscula o un guion bajo.

```ruby
def mostrar_mensaje
  mensaje = "Hola, mundo"  # Variable local a mostrar_mensaje
  puts mensaje
end

mostrar_mensaje  # Imprime "Hola, mundo"
# puts mensaje  # Esto causaría un error porque 'mensaje' no es accesible aquí
```

### Variables Globales

Las variables globales, por otro lado, están disponibles en todo el programa. Se indican con el prefijo `$` y deben usarse con precaución, ya que pueden ser modificadas desde cualquier parte del programa, lo que puede llevar a un código difícil de rastrear y mantener.

```ruby
$variable_global = "Accesible desde cualquier lugar"

def leer_variable_global
  puts $variable_global
end

leer_variable_global  # Imprime "Accesible desde cualquier lugar"
```

### Constantes

Las constantes se utilizan para almacenar datos que no deseas que cambien durante la ejecución de tu programa. En Ruby, las constantes se nombran con todas las letras en mayúsculas. Aunque Ruby permite cambiar el valor de una constante, te advertirá si intentas hacerlo.

```ruby
PI = 3.14159

def mostrar_pi
  puts PI
end

mostrar_pi  # Imprime 3.14159
# PI = 3.14  # Ruby emitirá una advertencia si intentas cambiar el valor de PI
```

---

Las variables y la asignación son fundamentales para cualquier programa Ruby. Entender la diferencia entre variables locales, globales y constantes, así como sus alcances y usos recomendados, es esencial para escribir código limpio y mantenible. 

[:arrow_backward:](07-Operadores.md) [:arrow_forward:](09-Bucles.md)