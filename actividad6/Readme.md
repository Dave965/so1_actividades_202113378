## Completely Fair Scheduler

Características principales:

1. **Equidad:** Una de las características más importantes del CFS es su objetivo de proporcionar una asignación justa y equitativa de los recursos de la CPU entre todos los procesos en ejecución. Esto significa que todos los procesos deben recibir una cantidad justa de tiempo de CPU, independientemente de su prioridad o carga de trabajo.

2. **Algoritmo basado en tiempo:** El CFS utiliza un algoritmo basado en el tiempo para asignar tiempo de CPU a los procesos. Cada proceso recibe una cuota de tiempo proporcional basada en el tiempo transcurrido desde que se ejecutó por última vez. Esto garantiza que los procesos que han recibido menos tiempo de CPU en el pasado tengan una prioridad más alta para ejecutarse en el futuro.

3. **Utilización del tiempo de ejecución como métrica:** En lugar de utilizar la prioridad estática de un proceso, el CFS utiliza el tiempo de ejecución del proceso como métrica para determinar su prioridad. Cuanto menos tiempo de CPU haya recibido un proceso en comparación con otros, mayor será su prioridad para ejecutarse.

Funcionamiento:

1. **Árbol de tiempo de ejecución (rbtree):** El CFS utiliza un árbol de tiempo de ejecución (rbtree) para organizar los procesos en función de su tiempo de ejecución. Los procesos se insertan en el árbol según su tiempo de ejecución y se programan para ejecutarse de acuerdo con este orden.

2. **Selección del próximo proceso a ejecutar:** Cuando se produce una interrupción de temporización o un cambio de contexto, el CFS selecciona el próximo proceso a ejecutar mirando el nodo con el menor tiempo de ejecución en el árbol de tiempo de ejecución. Este proceso se programa para ejecutarse y su tiempo de ejecución se actualiza en consecuencia.

3. **Actualización del tiempo de ejecución:** Después de que un proceso se haya ejecutado durante un período de tiempo, su tiempo de ejecución se actualiza para reflejar el tiempo transcurrido. Esto asegura que los procesos que han recibido menos tiempo de CPU tengan una mayor prioridad para ejecutarse en el futuro.

