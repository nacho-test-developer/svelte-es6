<script>
  const user = {
    name: 'John',
    email: 'mail@mail.com',
    age: 22,
    country: 'Mexico',
    profession: 'web developer'
  }

  const things = [
		{ id: 1, color: '#0d0887' },
		{ id: 2, color: '#6a00a8' },
		{ id: 3, color: '#b12a90' },
		{ id: 4, color: '#e16462' },
		{ id: 5, color: '#fca636' }
	];

  // partiendo de un objeto, puedo desesctructurar sus elementos a variables.
  // Según la posición que indique las variables
  const {name, email} = user
  const {id, color} = things

  // recibo desde la función el objeto
  // desestructuro el objeto indicando las propiedades que deseo obtener.
  const showInfo = ({name, profession}) => console.log(`${name} is a ${profession}`)

  showInfo(user)
</script>

<p>name: {name}</p>
<p>email: {email}</p>

<div class="grid">
  <div>
    <h2>keyed</h2>
    {#each things as thing (thing.id)}
      <span style='background: {thing.color}'>{thing.id}</span>
    {/each}
  </div>
  <div>
    <h2>Unkeyed</h2>
    {#each things as thing}
      <span style='background: {thing.color}'>{thing.color}</span>
    {/each}
  </div>
</div>

<style>
  .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-gap: 10px;
  }
  span {
		display: inline-block;
		padding: 0.2em 0.5em;
		margin: 0 0.2em 0.2em 0;
		width: 4em;
		text-align: center;
		border-radius: 0.2em;
		color: white;
	}
</style>