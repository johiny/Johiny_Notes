- son las strings que escribías con las backtick resulta que tienen un poder mucho mayor de lo que parecían ya que se puede colocar por delante de ellas una función que las procese/ tome como argumento y haga muchas mas cosas con ella.
- ***Template Literals - String Default*** #code
  ```javascript
  `hola ${Nombre}`
  ```
- ***Template Literals - Custom Function*** #code
  ```javascript
  let custom = (strings,nombre) => {
    return strings[0] + nombre +  " eres tonto"
  }
  custom`hola ${Nombre}`
  // hola paco eres tonto
  ```
	- la función de arriba coge todas las strings como su primer argumento y el resto de variables como los siguientes.