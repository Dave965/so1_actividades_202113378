```c
#include <stdio.h>
#include <unistd.h>
#include <pthread.h>

void *thread_function(void *arg) {
    printf("hilo creado\n");
    return NULL;
}

int main() {
    pid_t pid;
    pthread_t tid;
    int procesos_unicos = 0;
    int hilos_unicos = 0;

    pid = fork();
    if (pid == 0) { /* child process */
        procesos_unicos++;
        fork();
        pthread_create(&tid, NULL, thread_function, NULL);
         hilos_unicos++;
    }
    fork();

    printf("hijos unicos: %d\n", procesos_unicos);
    printf("hilos unicos: %d\n",  hilos_unicos);

    return 0;
}
```


a) ¿Cuántos procesos únicos son creados?
- Para calcular el número de procesos únicos, podemos contar el número de veces que se incrementa la variable `procesos_unicos`. este se incrementa solo en el proceso hijo directo, por lo que el número de procesos únicos será 1.

b) ¿Cuántos hilos únicos son creados?
- Para calcular el número de hilos únicos, podemos contar el número de veces que se llama a `pthread_create()`. Este se llama solo en el proceso hijo directo, por lo que el número de hilos únicos será 1.

Por lo tanto, las respuestas a las preguntas son:
a) 1 proceso único creado.
b) 1 hilo único creado.