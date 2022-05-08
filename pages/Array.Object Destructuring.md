- destructurar es bastante útil cuando queremos solo cierta data de un objeto u array.
- ***Array and object destructuring*** #code
  ```javascript
  let frutas = ["manzana", "pera" , "papaya"]
  let [fruta1,fruta2] = frutas
  // i will get manzana and pera the first two index elements
  let frutas = {"fruta2" : "manzana", "fruta1" : "pera" ,"fruta3" : "papaya"}
  let {fruta1,fruta2} = frutas
  // i will get pera and manzana because the index order doesn't mind anymore.
  ```