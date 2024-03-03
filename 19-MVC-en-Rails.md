## MVC en Rails

### Modelo

Los **Modelos** en Rails representan la capa de datos y la lógica de negocio de la aplicación. Se encargan de interactuar con la base de datos, realizar validaciones y gestionar las relaciones entre los diferentes modelos. Los modelos en Rails heredan de `ActiveRecord::Base`, lo que proporciona una gran cantidad de funcionalidades para manipular los datos de la aplicación.

Por ejemplo, si tienes una aplicación con usuarios, definirías un modelo `User` para representar a los usuarios y manejar la lógica relacionada con ellos.

```ruby
class User < ApplicationRecord
  # Aquí iría la lógica relacionada con los usuarios
end
```

### Vista

Las **Vistas** en Rails se encargan de la presentación de datos, es decir, lo que el usuario ve en su navegador. Las vistas en Rails suelen ser archivos HTML con código Ruby embebido (archivos `.html.erb`) que permiten insertar dinámicamente contenido en la página web basado en los datos proporcionados por los controladores.

```erb
<!-- app/views/users/show.html.erb -->
<p>Nombre de Usuario: <%= @user.name %></p>
```

### Controlador

Los **Controladores** actúan como intermediarios entre modelos y vistas. Reciben las peticiones del usuario (por ejemplo, a través de un navegador web), interactúan con los modelos para obtener o guardar datos, y luego eligen una vista para renderizar la salida.

```ruby
class UsersController < ApplicationController
  def show
    @user = User.find(params[:id])
  end
end
```

En este ejemplo, el controlador `UsersController` maneja la acción `show`, que busca un usuario por su ID y luego presenta los datos del usuario a través de la vista asociada.

---

### Flujo de Trabajo en MVC

1. **Petición del Usuario**: Todo comienza con una petición del usuario, la cual es recibida por el router de Rails.
2. **Router**: El router determina a qué controlador debe dirigirse la petición, basándose en la URL y el método HTTP.
3. **Controlador**: El controlador recibe la petición y decide qué hacer con ella. Puede solicitar información de un modelo y decidir con qué vista responder.
4. **Modelo**: Si es necesario, el controlador interactúa con el modelo, que a su vez puede realizar consultas a la base de datos.
5. **Vista**: Finalmente, el controlador pasa los datos a la vista, que se renderiza y se envía al cliente como una respuesta HTTP.

Este flujo asegura una separación clara de responsabilidades dentro de la aplicación, facilitando el desarrollo y mantenimiento de código complejo. El patrón MVC, combinado con las convenciones y la estructura que Rails proporciona, permite a los desarrolladores construir aplicaciones web robustas y escalables de manera eficiente.

---

El patrón Modelo-Vista-Controlador (MVC) es fundamental para el desarrollo de aplicaciones web en Rails. Al seguir este patrón, puedes mantener tu código organizado y modular, lo que facilita la colaboración y el mantenimiento a largo plazo. Además, Rails proporciona herramientas y convenciones que hacen que trabajar con MVC sea sencillo y efectivo.

[:arrow_heading_up: Regresar al inicio del documento](#ruby-on-rails)