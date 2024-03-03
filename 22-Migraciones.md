## Migraciones en Ruby on Rails

### ¿Qué son las Migraciones?

Las migraciones son scripts escritos en Ruby que cambian la estructura de la base de datos de tu aplicación. Esto incluye crear o borrar tablas, añadir o eliminar columnas de una tabla, cambiar tipos de datos de columnas, entre otros. Cada migración modifica la base de datos desde un estado a otro y Rails mantiene un registro de qué migraciones se han ejecutado, asegurándose de que solo se ejecuten una vez.

### Crear una Migración

Para crear una migración, puedes usar el comando `rails generate migration`, seguido del nombre de la migración. El nombre de la migración debe describir la acción que va a realizar, utilizando verbos en pasado para mantener la convención. Rails generará un archivo de migración en el directorio `db/migrate` con un timestamp en el nombre para garantizar el orden correcto de ejecución.

Por ejemplo, para añadir una columna de `email` a una tabla de `users`, podrías ejecutar:

```sh
rails generate migration AddEmailToUsers email:string
```

Este comando genera un archivo de migración que contiene un método `change` con las instrucciones para añadir la columna `email`.

### Ejecutar Migraciones

Para aplicar la migración y modificar la base de datos, ejecuta:

```sh
rails db:migrate
```

Rails buscará en el directorio `db/migrate` cualquier migración que no haya sido ejecutada previamente y ejecutará las instrucciones definidas en el método `change` (o `up` si estás especificando separadamente los métodos `up` y `down` para migraciones más complejas).

### Revertir Migraciones

Si necesitas deshacer una migración, puedes usar:

```sh
rails db:rollback
```

Este comando revertirá la última migración ejecutada. Si necesitas revertir más de una migración, puedes especificar cuántas migraciones revertir con el parámetro `STEP`:

```sh
rails db:rollback STEP=2
```

### Modificar una Migración

Si una migración aún no ha sido ejecutada por otros desarrolladores o en producción, puedes modificarla directamente. Sin embargo, si la migración ya ha sido aplicada, es mejor crear una nueva migración para realizar los cambios necesarios.

---

Las migraciones son una herramienta esencial en Ruby on Rails que facilita el mantenimiento y la evolución de la base de datos de tu aplicación. Al usar migraciones, mantienes un registro claro de los cambios estructurales, permitiendo que tu aplicación evolucione de manera segura y controlada.

[:arrow_backward:](21-BBDD.md) [:arrow_forward:](23-Modelos.md)