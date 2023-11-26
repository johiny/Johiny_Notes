- Delimitan lo que puede hacer un archivo según el usuario.
- un típico conjunto de permisos en Linux se ve de esta forma:
  ![Deciphering Linux File System Permissions - Pressidium Hosting](https://pressidium.com/wp-content/uploads/2017/02/Pressidium_blogpost_23_02_2017_Blog-post-1.png)
- Cada archivo tiene en su inicio un - o un d el cual identifica si estamos trabajando con un archivo (-) o un directory (d) que vendría siendo como un grupo de archivos.
- Luego de este viene la parte chida la cual esta dividida en 3 en grupos de 3 caracteres, estos caracteres son r (read), w (write), x (execute), si algunos de estos caracteres falta y esta un guion (-) a su vez se entiende que ese grupo no tiene ese permiso, como puedes ver en el grafico superior estos grupos son, primero el usuario creador o dueño actual del archivo, segundo el grupo principal del usuario, tercero cualquier otro usuario.
- Sabiendo leer esos nueve caracteres podrás saber rápidamente que puede hacer un archivo y quien lo puede hacer.
- Estos se cambiar con el comando [[Chmod]] y puedes cambiar el dueño del archivo con [[Chown]]