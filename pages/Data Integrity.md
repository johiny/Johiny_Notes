- La integridad de los datos consiste en siempre estar observando si los datos con los que estamos trabajando son válidos, están completos y limpios. Estas tres características nos ayudan a evitar resultados erróneos en nuestros análisis.
  Imagina que te compras una nueva bicicleta y esta lamentablemente puede tener 3 de estos problemas:
	- Tiene una parte de mas que no pertenece a la bicicleta
	- Tiene una parte errónea que no debería ir ahí
	- No tiene una parte literalmente
- Cada uno de estos problemas podría llevar a consecuencias que no quieres por eso tendrás que cambiar, eliminar o agregar esa parte para que tu bicicleta/análisis funcione como debe funcionar.
- Estos problemas son un claro caso de [[Data Errors / Not Enough Data]]
- Pero como analista de datos como puedo saber cual es la pieza que esta mal o que falta?, hay muchas maneras que iras aprendiendo con el tiempo, una tabla rápida con distintas cualidades que puedes verificar en los datos es esta.
  | **Restricciones de datos** | Definición | Ejemplos |
  | ---- | ---- | ---- |
  | **Tipo de datos** | Los valores deben ser de un tipo específico: fecha, número, porcentaje, datos Booleanos, etc. | Si el tipo de datos es una fecha, un número único como el 30 no cumpliría la restricción y sería inválido |
  | **Rango de datos** | Los valores respetan un rango de valores máximos y mínimos predefinidos | Si el rango de datos es de 10 a 20, el valor 30 no cumpliría la restricción y sería inválido |
  | **Obligatoriedad** | Los valores no pueden quedar en blanco o vacíos | Si el dato de la edad aparece en un campo obligatorio, se deberá completar |
  | **Dato único** | Estos valores no pueden tener un duplicado | Dos personas no pueden tener el mismo número de teléfono dentro de la misma área de servicio |
  | **Patrones de expresiones regulares (regex)** | Los valores deben coincidir con un patrón prescrito | Un número de teléfono debe coincidir con el patrón xxx-xxx-xxxx (no se permiten otros caracteres) |
  | **Validación de campos cruzados** | Se pueden cumplir algunas condiciones específicas de campos múltiples | Los valores son porcentajes y los valores de campos múltiples deben sumar hasta 100% |
  | **Clave primaria** | (Para bases de datos solamente) Debe haber un valor único por columna. | Una tabla de base de datos no puede tener dos filas con el mismo valor de clave primaria. Una clave primaria es un identificador en una base de datos que hace referencia a una columna en la que cada valor es único. Se puede encontrar más información sobre claves primarias y claves externas en las secciones que siguen en este mismo programa. |
  | **Definir membresía** | (Para bases de datos solamente) Los valores de una columna deben provenir de un conjunto de valores específicos  | El valor para la columna debe ser Sí, No o No Aplicable |
  | **Clave externa** | (Para bases de datos solamente) Deben completarse valores únicos por columna que provengan de una columna de otra tabla | En una base de datos de contribuyentes impositivos de los Estados Unidos, la columna Estado debe incluir un estado o territorio válido con un conjunto de valores aceptables definido en una tabla separada de Estados. |
  | **Exactitud** | Grado de conformidad de los datos con respecto a la entidad real que se mide o describe | Si los valores de los códigos postales son validados por la calle, mejora la exactitud de los datos. |
  | **Exhaustividad** | Grado en que los datos contienen todas las medidas o componentes deseados | Si los datos sobre perfiles personales requieren el color de cabello o de ojos, y se completan ambos, el dato será exhaustivo. |
  | **Coherencia** | Grado de repetibilidad de los datos desde diferentes puntos de entrada o recopilación | Si un cliente tiene el mismo domicilio en las bases de datos de ventas y de reparaciones, el dato es coherente. |
- Siguiendo estas pausas si hay datos incompletos, incorrectos o irrelevantes para el problema que estas tratando de resolver, estos datos son llamados [[Dirty Data]]
- Al igual que en el desarrollo de software donde se utiliza [[Git]] o se crea una documentación para saber como funciona o como ha cambiado tu código en el análisis de datos no es diferente ya que tienes que documentar todo lo que haces con el dataset, para dar un paso atrás si quitaste o cambiaste algo que estaba bien como estaba, además de eso tener todo documentado te ayudara a tener reportes muy buenos con los que le darás confianza a los stakeholders u a otros miembros de la organización.
- Para llevar esa historia puedes utilizar un [[Changelog]], hoy en día casi todo software de manipulación de datos tiene un historial de cambios incorporado entonces no tendras que preocuparte por hacerlo manualmente, pero esto trae un problema! aunque el historial de cambios guarda los cambios no guarda el porque de los cambios ahí ya dependerá nuevamente de ti que documentes porque hiciste o se hizo cierto cambio este registro también puede contener [[Meta Datos]] sobre ese cambio agregándole aun más contexto a cualquier cambio.
- pero como sabemos si después de hacer toda la limpieza nuestros datos ya son [[Clean Data]]?
  siempre después de terminar una limpieza es excelente sentarse volver a pensar en el problema que queremos solucionar , en el objetivo del proyecto y dar una nueva chequeada al dataset con esos pensamientos en mente, con eso veremos si algún dato nos quedo sin limpiar o si debemos cambiar algo mas para lo que el proyecto necesita, también podemos comparar el dataset limpiado con su original sin limpiar.
- Aunque la verificación de la limpieza varia mucho entre cada proyecto y sus necesidades aqui tienes una lista comun de cosas a verificar:
	- **Fuentes de errores:** ¿Utilizaste las herramientas y las funciones correctas para encontrar la fuente de los errores en tu conjunto de datos?
	- **Datos nulos:** ¿Buscaste DATOS NULOS utilizando el formato condicional y los filtros?
	- **Palabras mal escritas:** ¿Localizaste todas las palabras mal escritas?
	- **Números mal escritos:** ¿Revisaste dos veces que tus datos numéricos hayan sido ingresados correctamente?
	- **Espacios y caracteres extra:** ¿Eliminaste los espacios y caracteres extra utilizando la función **TRIM**?
	- **Duplicados:** ¿Eliminaste los duplicados en las hojas de cálculo utilizando la función **Quitar duplicados** o **DISTINCT **en SQL?
	- **Error de coincidencia de tipos de datos:** ¿Revisaste que los datos numéricos, las fechas y las cadenas de datos tengan el tipo correcto?
	- **Cadenas desordenadas (incoherentes):** ¿Te aseguraste de que todas tus cadenas sean coherentes y significativas?
	- **Formatos de fecha desordenados (incoherentes):** ¿Diste formato a las fechas de forma uniforme en todo el conjunto de datos?
	- **Etiquetas engañosas de variables (columnas):** ¿Asignaste nombres significativos a tus columnas?
	- **Datos truncados:**¿Comprobaste si había datos truncados o faltantes que debieran ser corregidos?
	- **Lógica de negocios:** ¿Comprobaste si los datos tienen sentido dados tus conocimientos del negocio?