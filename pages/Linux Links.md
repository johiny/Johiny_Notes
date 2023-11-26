- Un link o enlace en Linux puede ser de 2 tipos
- Hard Link: es un archivo que apunta hacia otro archivo y todo su contenido estará compartido, si se borra uno el otro seguirá existiendo como una especie copia, esto no quiere decir que ocupe más espacio si no que hay 2 enlaces apuntando a un mismo punto en memoria por eso si se borra uno no se borra el contenido y se puede seguir accediendo desde el otro.
- Symbolic Link: es un archivo que apunta hacia otro archivo pero a diferencia del hard link este no actúa como una especie de copia sino solo como un enlace si se borra el original o se altera su nombre/ruta el enlace ya no tendrá los datos ya que estaría apuntando a un archivo inexistente.
- Parece ser que su mayor diferencia además de su comportamiento principal es que los hard links y los archivos a los que apuntan tienen que estar en el mismo sistema de archivos mientras que los symbolic links pueden apuntar a archivos que estén en otros sistemas de archivos.