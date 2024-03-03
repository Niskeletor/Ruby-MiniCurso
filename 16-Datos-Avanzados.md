## Enumerables y Métodos Enumerable

Ruby proporciona el módulo `Enumerable`, que es uno de los más poderosos y utilizados en la programación Ruby. Este módulo ofrece un conjunto de métodos para recorrer, buscar, ordenar y manipular colecciones como arrays, hashes, y rangos.

```ruby
[1, 2, 3, 4, 5].each do |numero|
  puts numero
end

# Encuentra el primer número mayor que 3
puts [1, 2, 3, 4, 5].find { |numero| numero > 3 }  # => 4

# Suma todos los números
puts [1, 2, 3, 4, 5].reduce(:+)  # => 15
```

Los métodos proporcionados por `Enumerable` son extremadamente útiles para trabajar con datos de colecciones de manera eficiente.

## Expresiones Regulares (Regex)

Las expresiones regulares son una herramienta poderosa para el manejo de cadenas de texto, permitiéndote buscar, reemplazar, y validar texto basado en patrones específicos.

```ruby
texto = "Ruby es fantástico."

# Buscar si el texto contiene "Ruby"
puts !!texto.match(/Ruby/)  # => true

# Reemplazar "fantástico" por "increíble"
nuevo_texto = texto.gsub("fantástico", "increíble")
puts nuevo_texto  # => "Ruby es increíble."
```

Ruby maneja las expresiones regulares de manera muy integrada, facilitando el trabajo con patrones complejos de texto.

## File I/O

### Lectura de Archivos

Ruby facilita la lectura de archivos, permitiéndote acceder al contenido de un archivo en tu sistema de archivos para su procesamiento.

```ruby
File.open("ejemplo.txt", "r") do |archivo|
  contenido = archivo.read
  puts contenido
end
```

### Escritura de Archivos

De manera similar, puedes escribir en archivos para guardar datos. Esto es útil para una variedad de tareas, desde la persistencia de datos hasta la generación de archivos de configuración.

```ruby
File.open("salida.txt", "w") do |archivo|
  archivo.puts "Ruby hace fácil escribir en archivos."
end
```

---

Estos conceptos son esenciales para cualquier programador Ruby, ya que proporcionan las herramientas necesarias para manipular datos, trabajar con texto de manera avanzada y manejar archivos, tres tareas comunes en muchos programas.

 [:arrow_backward:](15-Modulos.md) [:arrow_forward:](17-Testing.md)