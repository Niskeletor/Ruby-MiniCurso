
## Instalación y configuración del entorno

Instalar Ruby y configurar tu entorno de desarrollo es el primer paso para sumergirte en el mundo de la programación con Ruby. Afortunadamente, Ruby es amigable con la mayoría de los sistemas operativos, y aquí te guiaré a través del proceso para Windows, macOS y Linux.

### **Windows**

Para los usuarios de Windows, RubyInstaller ofrece la forma más sencilla de obtener Ruby en tu máquina. Sigue estos pasos:

1. Visita [RubyInstaller](https://rubyinstaller.org/) y descarga la versión más reciente acorde a tu sistema.
2. Ejecuta el archivo descargado y sigue las instrucciones del asistente de instalación. Asegúrate de marcar la casilla que dice "Add Ruby executables to your PATH" para facilitar la ejecución de Ruby desde la línea de comandos.
3. Una vez instalado, abre una terminal y escribe `ruby -v` para verificar que Ruby se ha instalado correctamente.

### **macOS**

macOS viene con Ruby instalado por defecto, pero es posible que desees instalar una versión más reciente. Homebrew, el gestor de paquetes para macOS, facilita esta tarea:

1. Si aún no tienes Homebrew, instálalo ejecutando en la Terminal:
   ```
   /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
   ```
2. Luego, instala Ruby con Homebrew:
   ```
   brew install ruby
   ```
3. Para asegurarte de que la versión de Ruby gestionada por Homebrew tenga prioridad en el PATH, añade lo siguiente a tu archivo `.bash_profile` o `.zshrc`:
   ```
   export PATH="/usr/local/opt/ruby/bin:$PATH"
   ```
4. Verifica la instalación con `ruby -v`.

### **Linux**

En Linux, el gestor de paquetes de tu distribución facilitará la instalación de Ruby. Por ejemplo, en sistemas basados en Debian (como Ubuntu), puedes usar `apt`:

1. Abre una terminal y actualiza tu lista de paquetes:
   ```
   sudo apt update
   ```
2. Instala Ruby:
   ```
   sudo apt install ruby-full
   ```
3. Verifica que Ruby se ha instalado correctamente con `ruby -v`.

### **Configurando tu entorno de desarrollo**

Independientemente del sistema operativo, te recomiendo instalar un buen editor de texto diseñado para programación, como Visual Studio Code, Sublime Text o Atom. Estos editores ofrecen características como resaltado de sintaxis y autocompletado de código que hacen la programación más eficiente y agradable.

Con Ruby instalado y tu editor de texto listo, estás preparado para empezar a explorar el maravilloso mundo de la programación con Ruby. ¡El viaje acaba de comenzar!


---
[:arrow_backward:](02-Historia-Ruby.md) [:arrow_forward:](04-Sintaxis.md)

[]: # (END)
[]: # (Hasta aquí el capítulo 3)

[]: # (START