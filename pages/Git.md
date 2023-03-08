- El sistema de control de versiones mas popular.
- Buena grafica para entender las diferentes áreas/etapas y cual de estas afectan los comandos al trabajar con git:
  ![como-funciona-staging-y-staging-area.png](https://static.platzi.com/media/user_upload/estados-git-0acb84f7-5080-4098-99d9-59012a3b8e86-e5b46dbb-9bab-4d7c-aa74-c055ffcde639.jpg)
- Buena grafica de como se llega a utilizar las [[Branches]] es un ambiente profesional cotidiano:
  ![https://static.platzi.com/media/user_upload/ramas-branch-en-git-7e72b407-90cc-4b90-8de1-738b155764eb.jpg](https://static.platzi.com/media/user_upload/ramas-branch-en-git-7e72b407-90cc-4b90-8de1-738b155764eb.jpg)
- la cabecera o Head es como un puntero que apunta sobre que commit esta ahora mismo activo en nuestro directorio, además cuando hacemos checkout a una rama esto nos lleva al ultimo commit de esta por defecto!, por eso el checkout funcionaba con commits o ramas, ahora entiendo que la cabecera no es:
- la versión mas actual de los archivos, o el ultimo commit del master, el head es el puntero que nos indica donde estamos ahora mismo en todo el mar de versiones de nuestros archivos.
- también si alguna vez te habías preguntado como hacían lo de las releases, es con tags en git se pueden agregar tags a cierto commit en especifico y luego esas tags son a las que les ponen el nombre de release v1, v2, v2.4, etc. las tags llevan al commit / código que estaba en algún momento en especifico.
- ***Git Tags*** #code
  ```bash
  git tag -a v1.4 -m "my version 1.4" # add new tag based on where is the head
  git tag -a v1.4 -m "my version 1.4" 9fceb02 # add a new tag based on the commit that is passed as a reference
  ```
- también sabias que git viene con un pequeño software para visualizar las ramas que tengas? se llama gitk muy curioso la verdad.
  ![image.png](../assets/image_1678232568990_0.png)
- algo mas avanzado y que en realidad no es de git si no de GitHub son los [[Pull Request]]
- Se pueden tener varios repositorios remotos enlazados con el repositorio local si estamos trabajando con un repo en el cual no somos colaboradores directos, se suele agregar este con el nombre upstream para descargar todas los últimos cambios que hayan hecho los dueños, con eso luego nosotros ya podemos cambiar algunas cosas y subirlo a nuestro repositorio clon/fork.