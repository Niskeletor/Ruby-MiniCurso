
## Tipos de Datos

Ruby es un lenguaje rico y expresivo, con una variedad de tipos de datos incorporados que te permiten manejar números, texto, y mucho más de manera intuitiva. Aquí exploraremos los tipos de datos más comunes en Ruby y cómo puedes utilizarlos en tus programas.

### Números

Ruby maneja tanto números enteros (`Integer`) como de punto flotante (`Float`). Puedes realizar operaciones matemáticas básicas con ellos, como suma, resta, multiplicación y división.

```ruby
entero = 42
flotante = 3.14

suma = entero + flotante  # 45.14
```

### Cadenas de Texto (Strings)

Las cadenas de texto, o `String`, son secuencias de caracteres utilizadas para manejar texto. Puedes concatenarlas, interpolar variables dentro de ellas, y aplicarles métodos para manipularlas.

```ruby
saludo = "Hola, "
nombre = "Nis"

mensaje = "#{saludo}#{nombre}"  # "Hola, Nis"
```

### Símbolos

Los `Symbol` son cadenas inmutables utilizadas frecuentemente como identificadores. A diferencia de las strings, cada símbolo es único, lo que los hace más eficientes para ciertos usos, como las claves en hashes.

```ruby
color_preferido = :azul
```

### Booleanos

Ruby utiliza `true` y `false` para representar valores booleanos, permitiéndote realizar operaciones lógicas y controlar el flujo de tu programa.

```ruby
verdadero = true
falso = false
```

### Rangos

Los `Range` representan una secuencia de valores. Son especialmente útiles para crear secuencias numéricas o iterar sobre un conjunto de valores.

```ruby
dias_de_la_semana = 1..7
```

### Arreglos

Los `Array` son colecciones ordenadas de objetos. Puedes almacenar cualquier tipo de objeto en un arreglo y acceder a ellos por su índice.

```ruby
piedresPrecioses = ["rubi", "topacio", "esmeralda", "zafiro", "diamante"]
```

### Hashes

Los `Hash` son colecciones de pares clave-valor. Son similares a los arreglos, pero accedes a sus valores utilizando claves únicas en lugar de índices numéricos.

```ruby
persona = { nombre: "Nis", profesion: "Desarrollador" }
```
---
Los tipos de datos son fundamentales para cualquier programa Ruby. Comprender cómo manejar números, texto, y otros tipos de datos te permitirá escribir programas más expresivos y eficientes.

[:arrow_backward:](04-Sintaxis.md) [:arrow_forward:](06-Métodos.md)