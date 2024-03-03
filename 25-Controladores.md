## Controladores en Ruby on Rails

### Creación de Controladores

Para crear un controlador en Rails, puedes usar el generador de controladores que proporciona una forma rápida de crear tanto el controlador como las vistas asociadas y las rutas. Por ejemplo, para crear un controlador `Users` con acciones `new` y `show`, ejecutarías:

```sh
rails generate controller Users new show
```

Este comando crea un archivo de controlador en `app/controllers/users_controller.rb` con métodos para `new` y `show`, vistas correspondientes en `app/views/users/`, y rutas en `config/routes.rb`.

### Estructura de un Controlador

Un archivo de controlador en Rails contiene una clase que hereda de `ApplicationController`. Dentro de esta clase, defines métodos que corresponden a las acciones que puede realizar este controlador.

```ruby
class UsersController < ApplicationController
  def show
    @user = User.find(params[:id])
  end
end
```

En este ejemplo, la acción `show` busca un usuario por `id` y lo asigna a una variable de instancia `@user`, que luego se puede acceder en la vista correspondiente.

### Filtros

Los filtros en Rails permiten ejecutar lógica antes, después o "alrededor" de las acciones de un controlador. Son útiles para tareas como la autenticación de usuarios, la carga de recursos antes de ejecutar acciones o el registro.

```ruby
class UsersController < ApplicationController
  before_action :find_user, only: [:show, :edit, :update, :destroy]

  private
    def find_user
      @user = User.find(params[:id])
    end
end
```

### Parámetros Fuertemente Tipados

Rails utiliza parámetros fuertemente tipados (strong parameters) para prevenir la asignación masiva no deseada de atributos. Esto te obliga a especificar explícitamente qué parámetros están permitidos para la creación o actualización de modelos.

```ruby
class UsersController < ApplicationController
  def create
    @user = User.new(user_params)
    if @user.save
      # Trata el éxito
    else
      # Trata el fracaso
    end
  end

  private
    def user_params
      params.require(:user).permit(:name, :email)
    end
end
```

### Rutas y Acciones

Rails asocia rutas con acciones en los controladores mediante el archivo `config/routes.rb`. Puedes definir rutas específicas para cada acción o utilizar rutas de recursos para generar automáticamente rutas estándar CRUD (crear, leer, actualizar, borrar) para un controlador.

```ruby
resources :users
```

---

Los controladores son una pieza clave en la arquitectura de Rails, proporcionando una forma clara y organizada de gestionar la interacción entre el usuario y la aplicación. Al comprender y utilizar correctamente los controladores, puedes construir aplicaciones web complejas y eficientes.
