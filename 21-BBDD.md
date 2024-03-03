## Bases de Datos en Ruby on Rails

### Configuración

Rails soporta una variedad de sistemas de gestión de bases de datos (DBMS), como SQLite, PostgreSQL, y MySQL. La configuración de la base de datos de tu aplicación se encuentra en el archivo `config/database.yml`. Por defecto, Rails configura SQLite para el entorno de desarrollo debido a su simplicidad y facilidad de uso.

Para configurar otro DBMS, debes modificar este archivo con los detalles de conexión adecuados para tu entorno de desarrollo, prueba, y producción.

### Migraciones

Las migraciones en Rails son una manera potente y versionada de alterar la estructura de la base de datos de tu aplicación con el tiempo. Te permiten evolucionar la base de datos de tu aplicación de manera controlada y segura. Para crear una nueva migración, puedes utilizar el generador de migraciones:

```sh
rails generate migration NombreDeLaMigracion
```

Por ejemplo, para crear una tabla `users`, podrías nombrar tu migración algo así:

```sh
rails generate migration CreateUsers
```

Rails generará un archivo de migración en `db/migrate/` con un timestamp en el nombre para garantizar el orden de las migraciones.

Dentro de este archivo, puedes definir cómo cambiar la estructura de la base de datos, por ejemplo:

```ruby
class CreateUsers < ActiveRecord::Migration[6.0]
  def change
    create_table :users do |t|
      t.string :name
      t.string :email

      t.timestamps
    end
  end
end
```

Para aplicar la migración y actualizar la base de datos, ejecuta:

```sh
rails db:migrate
```

### ActiveRecord

ActiveRecord es el ORM (Object-Relational Mapping) incluido en Rails, que te permite interactuar con la base de datos de una manera orientada a objetos. Con ActiveRecord, puedes realizar consultas, insertar, actualizar y eliminar registros sin escribir SQL crudo.

Por ejemplo, para crear un nuevo usuario, puedes hacer:

```ruby
User.create(name: "Nis", email: "nis@example.com")
```

### Seeds

Rails también proporciona una manera de alimentar tu base de datos con datos iniciales a través de archivos de semillas (seeds). Esto es útil para poblar tu base de datos con datos de prueba o inicializarla con información necesaria para que tu aplicación funcione. Puedes encontrar el archivo de seeds en `db/seeds.rb`.

Para ejecutar tus seeds, simplemente ejecuta:

```sh
rails db:seed
```

---

Trabajar con bases de datos en Rails es eficiente y simplificado gracias a herramientas como ActiveRecord y las migraciones. Estas herramientas te ayudan a mantener tu código y estructura de base de datos organizados, versionados, y en sincronía con el desarrollo de tu aplicación.

[:arrow_backward:](20-Proyecto.md) [:arrow_forward:](22-Migraciones.md)