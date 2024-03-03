## Modelos en Ruby on Rails

### Creación de Modelos

Para crear un modelo en Rails, generalmente usas un generador de línea de comandos. Este proceso crea un archivo de modelo en `app/models` y opcionalmente, una migración en `db/migrate` para definir la estructura de la tabla correspondiente en la base de datos.

Por ejemplo, para crear un modelo `User` con una migración para una tabla `users`, ejecutarías:

```sh
rails generate model User name:string email:string
```

Este comando crea un archivo de modelo `user.rb` y una migración para añadir la tabla `users` con columnas `name` y `email`.

### Estructura de un Modelo

Un archivo de modelo en Rails contiene la definición de una clase Ruby que hereda de `ApplicationRecord`, que a su vez hereda de `ActiveRecord::Base`. Esto conecta tu modelo con la base de datos y te proporciona una gran cantidad de funcionalidades para trabajar con esos datos.

```ruby
class User < ApplicationRecord
  # Aquí puedes añadir validaciones, relaciones, y métodos personalizados
end
```

### Validaciones

Rails te permite definir validaciones dentro de tus modelos para asegurar que los datos sean correctos antes de ser guardados en la base de datos. Por ejemplo:

```ruby
class User < ApplicationRecord
  validates :name, presence: true
  validates :email, presence: true, uniqueness: true
end
```

### Relaciones

Los modelos pueden definir relaciones entre sí que reflejan las relaciones entre las tablas en la base de datos, como `has_many`, `belongs_to`, y `has_one`.

```ruby
class User < ApplicationRecord
  has_many :posts
end

class Post < ApplicationRecord
  belongs_to :user
end
```

### Métodos Personalizados

Además de las validaciones y las relaciones, puedes definir tus propios métodos dentro de los modelos para encapsular comportamientos específicos relacionados con los datos.

```ruby
class User < ApplicationRecord
  def full_name
    "#{first_name} #{last_name}"
  end
end
```

---

Los modelos en Ruby on Rails son herramientas poderosas que te permiten manejar la lógica de negocio y la interacción con la base de datos de manera eficiente y organizada. Al aprovechar las características de ActiveRecord, Rails hace que trabajar con bases de datos sea intuitivo y flexible, permitiéndote centrarte en construir las funcionalidades de tu aplicación.

[:arrow_backward:](22-Migraciones.md) [:arrow_forward:](24-Vistas.md)