### Tipos de Kernel y sus diferencias:

- **Monolítico:**
  En un kernel monolítico, todas las funciones del sistema operativo se ejecutan en el espacio del núcleo. Esto significa que todos los servicios del sistema operativo, como la gestión de memoria, el sistema de archivos y los controladores de dispositivos, se ejecutan en un solo bloque de código.

- **Microkernel:**
  Un kernel microkernel, en cambio, minimiza la cantidad de funciones que se ejecutan en el espacio del núcleo y desplaza algunas funciones a los procesos del espacio del usuario. Esto ayuda a mejorar la estabilidad y la modularidad del sistema operativo.

- **Híbrido:**
  Como su nombre indica, un kernel híbrido combina características de los kernels monolíticos y microkernels. Algunas funciones críticas se ejecutan en el espacio del núcleo, mientras que otras se ejecutan en el espacio del usuario.

### User vs Kernel Mode:

- **User Mode:**
  En este modo, el software se ejecuta con un conjunto restringido de instrucciones y direcciones de memoria. Las aplicaciones de usuario normales se ejecutan en este modo y no tienen acceso directo al hardware ni a las instrucciones privilegiadas del procesador.

- **Kernel Mode:**
  En este modo, el software tiene acceso completo a las instrucciones y al hardware del sistema. El núcleo del sistema operativo se ejecuta en este modo y tiene control total sobre el hardware.

### Interruptions vs Traps:

- **Interrupts:**
  Son eventos que ocurren de manera asíncrona y que pueden interrumpir la ejecución normal de un programa. Las interrupciones son manejadas por el sistema operativo para realizar tareas como gestionar la entrada/salida, manejar errores y gestionar eventos externos.

- **Traps:**
  También conocidas como excepciones, son eventos síncronos que ocurren durante la ejecución de un programa debido a condiciones excepcionales, como divisiones por cero o acceso a memoria no permitida. Las trampas permiten al sistema operativo manejar y corregir estas condiciones.