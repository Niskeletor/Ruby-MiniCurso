## Creación de un Proyecto en Ruby on Rails

### Requisitos Previos

Asegúrate de tener Ruby y Ruby on Rails instalados en tu sistema. Puedes verificar las versiones instaladas con los siguientes comandos en tu terminal:

```sh
ruby -v
rails -v
```

Si Rails no está instalado, puedes instalarlo con el siguiente comando de RubyGems:

```sh
gem install rails
```

### Crear un Nuevo Proyecto

Para crear un nuevo proyecto de Rails, abre una terminal y ejecuta el siguiente comando, donde `mi_app` es el nombre de tu aplicación:

```sh
rails new mi_app
```

Este comando generará una nueva carpeta llamada `mi_app` con toda la estructura de directorios de un proyecto Rails y también instalará las gemas necesarias especificadas en el `Gemfile`.

### Estructura del Proyecto

Dentro de tu proyecto de Rails, encontrarás varios directorios y archivos importantes:

- `app/`: Contiene los modelos, vistas, controladores, ayudantes, y activos para tu aplicación.
- `config/`: Contiene configuraciones de tu aplicación, incluyendo el enrutamiento.
- `db/`: Contiene todo relacionado con la base de datos, incluyendo migraciones y esquemas.
- `Gemfile`: Especifica las gemas (librerías) que tu aplicación necesita.
- `config/routes.rb`: Define las rutas de tu aplicación, mapeando URLs a controladores.

### Iniciar el Servidor

Para ver tu aplicación en acción, necesitas iniciar el servidor de Rails. Navega a la carpeta de tu proyecto (`mi_app`) en la terminal y ejecuta:

```sh
rails server
```

o simplemente:

```sh
rails s
```

Esto iniciará un servidor web local en el puerto 3000. Abre tu navegador y visita `http://localhost:3000` para ver la página de bienvenida de Rails.

---

Ahora ya se un proyecto de Ruby on Rails en marcha y listo para ser desarrollado. Desde aquí, puedes comenzar a agregar modelos, vistas, y controladores para construir la funcionalidad de tu aplicación web. Rails ofrece una amplia gama de herramientas y generadores que te ayudarán a agregar nuevas características rápidamente.