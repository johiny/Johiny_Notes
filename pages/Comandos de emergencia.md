- Aunque borres, mezcles, hagas rebase, renombres cualquier cosa que altere la historia, y pareciera que despareció o cambio de git log, hay un registro por encima de todos, el One-Above-All de Git.
- Este es el Git Reflog:
  ***Git Reflog*** #code
  ```bash
  git reflog #see everything that have happen in the repository
  ```
- con este comando literalmente puedes ver todo lo que ha pasado en el repositorio cada mínima acción hecha, no importa que la historia principal la línea temporal actual haya sido cambiada esos cambios estarán ahí.
- ahora que tienes el poder de ver todo aquello que ha sucedido desde el inicio de los tiempos que pasa si todo se fue al carajo y quieres devolver el universo a un estado donde todo estaba bien?
- para esto existe nuestro segundo comando de emergencia Git Reset:
  ***Git Reset*** #code
  ```bash
  git reset --HARD {ref_of_some_time_point} # get back in time and delete every change you have in the working directory
  git reset --SOFT {ref_of_some_time_point} # get back in time but preserve the changes you have in the working directory
  ```
- Como puedes observar arriba existen 2 variantes de este comando 1 que conserva los cambios que están staging y otro que no, casi siempre se usa el hard ya que si estas haciendo reset es porque las cosas están muy mal en el presente entonces es mejor dejarlo todo y volver al pasado.