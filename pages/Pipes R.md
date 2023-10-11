- las pipes en R son una herramienta bastante curiosa que soluciona un problema bastante común que seguramente habías visto en otros lenguajes de programación, las acciones que dependen de los resultados de otras acciones.
  a que me refiero con esto? a las situaciones donde los parámetros de una función vienen de los resultados de otra.
- Seguramente has tenido que hacer algo como esto muchas veces
- ***Function Results Sequence*** #code
  ```javascript
  const first_result = dosomething()
  const second_result = dosomenthing2(first_result)
  const final_result = dosomenthing3(second_result)
  ```
- seguramente para evitar esto habrás pensado también en la estrategia de nested functions
- ***Nested Functions*** #code
  ```javascript
  const final_result = dosomenthing3(dosomenthing2(dosomething()))
  ```
- como podrás notar con esta estrategia nos ahorramos la necesidad de usar variables que solo necesitaremos por unos momentos.
- Pero que tienen que ver las pipes con todo esto??, las pipes son la solución de R a este problema.
- ***R Pipes*** #code
  ```R
  final_result <- dosomething() %>%
  	dosometing2() %>%
  	dosometing3()
  #look every function come after another and its result is passed as argument to the other function like a pipeline!
  ```
- como puedes ver esta sintaxis es un poco extraña, pero lo que hace es crear una pipe donde el resultado de nuestra función anterior será pasado como argumento a la siguiente de manera automática como una linea de ensamblaje!.