<script>
  const myArray = ['Ignacio', 'Arguello', 'Argentina', 30]

  // partiendo de un arreglo, puedo desesctructurar sus elementos a variables.
  // Según la posición que indique las variables
  const [firstName, lastName, country, age] = myArray

  // recibo desde la función el array
  // desestructuro el array indicando las variable que deseo obtener.
  // puedo obter el 1º y último elemento dejando con espacios los que no necesito
  const myFunction = ([name, , ,edad]) => console.log(`${name} de ${edad} años`)

  myFunction(myArray)

</script>

<p>Last name: {lastName}</p>