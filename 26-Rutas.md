## Rutas en Ruby on Rails

El sistema de enrutamiento de Rails determina cómo las peticiones HTTP son respondidas por tu aplicación. Este sistema se define en el archivo `config/routes.rb`, donde mapeas URLs a controladores y acciones específicas.

### Definición de Rutas Simples

Para una acción `index` en un controlador `BooksController`, podrías definir una ruta así:

```ruby
get 'books/index', to: 'books#index'
```

Esto significa que cuando un usuario visita `http://tu_dominio.com/books/index`, Rails enviará esa petición al método `index` en `BooksController`.

### Recursos

Rails proporciona una forma más conveniente de generar rutas para acciones comunes en tus controladores utilizando el método `resources`. Por ejemplo:

```ruby
resources :books
```

Este único comando crea siete rutas diferentes en tu aplicación, cubriendo las acciones CRUD (Crear, Leer, Actualizar, Eliminar) típicas: `index`, `show`, `new`, `create`, `edit`, `update`, y `destroy`.

### Rutas Anidadas

Las rutas anidadas te permiten expresar relaciones jerárquicas en tu aplicación. Por ejemplo, si cada `book` tiene muchos `reviews`, puedes definir rutas anidadas así:

```ruby
resources :books do
  resources :reviews
end
```

Esto te permite construir URLs que reflejan la relación entre libros y reseñas, como `books/:book_id/reviews/:id`.

### Rutas Personalizadas

Para rutas que no se ajustan al patrón estándar RESTful o necesitas una URL específica, puedes definir rutas personalizadas:

```ruby
get 'books/search', to: 'books#search'
```

### Rutas con Parámetros

Las rutas pueden incluir parámetros, que se pasan a los controladores como parte de la petición. Por ejemplo:

```ruby
get 'books/:id', to: 'books#show'
```

En este caso, `:id` es un parámetro que permite a la ruta `show` del controlador `Books` mostrar el libro correspondiente al `id` proporcionado.

### Redirecciones

Rails también te permite definir redirecciones directamente en el archivo de rutas, lo cual es útil para mantener la organización de tus URLs o manejar URLs antiguas:

```ruby
get 'old-books', to: redirect('books')
```

---

Las rutas son una parte vital de cualquier aplicación Rails, proporcionando un mapeo flexible y potente entre las URLs de tu aplicación y su lógica de negocio. Aprovechar el sistema de enrutamiento de Rails te permite diseñar una experiencia de usuario clara y coherente.

[:arrow_backward:](25-Controladores.md) [:arrow_forward:](27-Despliegue.md)