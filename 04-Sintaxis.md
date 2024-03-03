
## Sintaxis básica de Ruby

Ruby es conocido por su sintaxis limpia y elegante, diseñada para ser intuitiva y fácil de leer, casi como pseudocódigo. Esto hace que sea un lenguaje de programación particularmente atractivo para principiantes, sin sacrificar la potencia y flexibilidad.

### Comentarios

Los comentarios en Ruby son fragmentos de texto que el intérprete ignora y se utilizan para añadir notas y explicaciones en el código, lo que resulta esencial para la legibilidad y mantenimiento del mismo. Ruby maneja los comentarios de una manera muy sencilla:

- **Comentarios de una línea** se crean usando el símbolo `#`. Todo lo que sigue a `#` en la misma línea es tratado como un comentario.

```ruby
# Esto es un comentario de una línea
puts "Hola, Rubioso!"  # Esto también es un comentario
```

- **Comentarios multilínea** en Ruby no tienen una sintaxis específica como tal, pero puedes utilizar el truco de `=begin` y `=end` para este propósito, aunque su uso no es recomendado en código moderno de Ruby por cuestiones de estilo.

```ruby
=begin
Este es un comentario
multilínea. No es tan común verlo,
pero puede ser útil para comentarios
muy largos.
=end
```

### Palabras reservadas

Ruby tiene un conjunto de palabras reservadas que son parte de la sintaxis del lenguaje y no pueden ser utilizadas como nombres de variables o métodos. Estas palabras tienen significados especiales y son cruciales para la estructura de los programas en Ruby. Algunas de las más importantes incluyen:

- `class`, `module`, `def` - Utilizadas para definir clases, módulos y métodos, respectivamente.
- `if`, `unless`, `else`, `elsif` - Controlan el flujo de ejecución mediante condiciones.
- `while`, `until`, `for` - Utilizadas en la construcción de bucles.
- `true`, `false`, `nil` - Representan los valores booleanos verdadero y falso, y el valor nulo, respectivamente.
- `begin`, `rescue`, `ensure`, `end` - Manejan bloques de código y excepciones.

La comprensión de estas palabras reservadas es esencial para escribir código Ruby efectivo y entender cómo Ruby interpreta las instrucciones que le proporcionas.

---

Las palabras reservadas y los comentarios son elementos fundamentales de la sintaxis de Ruby. Aprender a utilizarlos correctamente te ayudará a escribir código claro y legible, y a comprender mejor cómo Ruby interpreta tus instrucciones.

[:arrow_backward:](03-Configuracion.md) [:arrow_forward:](05-Tipos-Datos.md)