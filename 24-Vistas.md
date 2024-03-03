## Vistas en Ruby on Rails

### Estructura y Ubicación

Las vistas en Rails se almacenan en el directorio `app/views`. Este directorio está organizado en subdirectorios que corresponden a los controladores de tu aplicación, donde cada controlador tiene su propio subdirectorio. Dentro de estos subdirectorios, encontrarás archivos de vista que corresponden a las acciones definidas en el controlador.

Por ejemplo, para un controlador `UsersController` con una acción `show`, Rails esperará encontrar la vista en `app/views/users/show.html.erb`.

### ERB: Embedded Ruby

Rails utiliza ERB (Embedded Ruby) como su sistema de plantillas predeterminado. ERB te permite incrustar código Ruby dentro de documentos HTML para generar contenido dinámico. Las expresiones ERB se delimitan con etiquetas especiales:

- `<%= %>` para ejecutar código Ruby y mostrar su resultado.
- `<% %>` para ejecutar código Ruby sin mostrar su resultado.

Por ejemplo, para mostrar el nombre de un usuario en una vista:

```erb
<p>Bienvenido, <%= @user.name %></p>
```

### Partials

Los partials son vistas parciales que puedes reutilizar en diferentes vistas para evitar la duplicación de código. Los partials son especialmente útiles para componentes de la interfaz de usuario que se repiten, como barras de navegación, formularios y pies de página.

Para renderizar un partial llamado `_form.html.erb`:

```erb
<%= render 'form' %>
```

### Helpers

Rails proporciona helpers de vista, que son métodos diseñados para ayudarte a generar HTML de manera más sencilla. Existen helpers para formularios, enlaces, imágenes y más. También puedes definir tus propios helpers.

Por ejemplo, para crear un enlace en una vista:

```erb
<%= link_to 'Mi Perfil', user_path(@user) %>
```

### Layouts

Los layouts en Rails son plantillas que envuelven las vistas y proporcionan una estructura común para tus páginas, como los encabezados y pies de página que son comunes a toda la aplicación. Por defecto, Rails utiliza el archivo `application.html.erb` en `app/views/layouts` como el layout principal.

---

Las vistas son una parte fundamental de cualquier aplicación Rails, permitiéndote crear interfaces de usuario ricas y dinámicas. Al aprovechar las características de Rails como ERB, partials, helpers y layouts, puedes construir aplicaciones web complejas y atractivas de manera eficiente.

[:arrow_backward:](23-Modelos.md) [:arrow_forward:](24-Vistas.md)