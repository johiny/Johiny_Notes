- El Python para estadísticos que vienen de las matemáticas puras vamos a ver que tal es!
- R al contrario de [[Python]] que es un lenguaje multipropósito, R esta mas orientado a trabajar con datos y a la estadística es lo que se conoce como data-centric.
- Parece que una forma bastante popular de trabajar con R es R-Studio al igual que los [[Jupyter NoteBooks]] en Python
- al igual que en otros lenguajes de programación en R han surgido paquetes hechos por la comunidad para facilitar las cosas, famosos paquetes que todo el mundo utiliza como numpy o pandas en python, parece que ese puesto le pertenece a [[tidyverse]] en R.
- una buena manera de ver que hace una función en R es con la sintaxis
- ***Help Syntax*** #code
  ```R
  ?print()
  # will return the manual page of the print function
  ```
- esto funciona igualito al comando man de [[Linux]]
- En R como parece ser común entre los lenguajes de programación el operador de asignación es el "=" de toda la vida, pero no solo hay un operador de asignacion y además de eso el "=" no es el mas popular!, por ello seguramente por internet encontraras muchos ejemplo de R con esta sintaxis:
- ***Assignment Operator*** #code
  ```R
  my_variable <- "my value"
  # wtf is that?!
  ```
- Otra diferencia grande con otros lenguajes que hayas usado es que los vectores/arrays aunque se accede igual a sus elementos estos se inician con una función la función c, solo pueden ser de un tipo de dato y además de ello no empiezan en 0!! what??! what??!!.
- ***R Arrays*** #code
  ```R
  x <- c("manzana","pera","mora")
  x[1]
  #this will access "manzana " item!, what??! there is not 0 index!
  ```
- También se pueden crear los hermanos de los arrays las listas que son casi iguales excepto por su capacidad de poder almacenar diferentes tipos de datos estos se pueden crear con la función list()
- Por ultimo hay algo si bastante diferente y también bastante curioso sobre R las [[Pipes]]
- Como recordaras de la [[Data Science]] solo guiarnos por [[Estadísticos Descriptivos]] puede llevar a asunciones erróneas a cerca del dataset, como un promedio alterado por un outlier extremo, entonces si solo confiamos en los estadísticos de resumen seguramente acabemos mal interpretando lo que expresa ese dataset. Para esto R es muy bueno para hacer visualizaciones rápidamente y sacarnos esas dudas que dejan las primeras métricas estadísticas.
- En R también existe una curiosa función bastante interesante esta nos permite calcular el [[Bias]] que podría tener un dataset, suena sorprendente no?, parece que ser que esta función tiene sus fundamentos en  seguramente cosas muy complejas de la [[Estadística]] que en algún momento llegara a eso pero por ahora basta con que entiendas la abstracción y el objetivo de esta función.
- ***Bias Function*** #code
  ```R
  actual_values <- (2,6,8,19,0,3)
  predicted_values <- (1,2,67,12,6,5)
  bias(actual_values, predicted_values)
  # bias compare the actual values with the predicted values of a model to see if it or its dataset is biased and how much
  # near to 0 better
  ```