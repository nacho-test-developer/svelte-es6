<script>
  import { onMount } from 'svelte';
  
  export let title;

  const names = ['Carlos', 'Alejandro', 'nachito'];

  let result = []

  // Map - iterar una función por cada uno de los elementos
  const nameExtract = names.map(function(name) {
    console.log(name)
  })

  function cl(val) {
    if(val === 'nachito'){
      result.push(val)
    }
    console.log(`cl ${val}`)
  }

  // Arrow function
  // si es un solo parámetro, se puede no usar ()
  // si es en una línea se puede eliminar return y {}
  const nameExtract2 = names.map(name => cl(name))

  // console.log('dos: ',nameExtract2)
</script>

<h5>Welcomte to {title}!</h5>

<ul>
	{#each names as item, i}
  <li>{item}</li>
	{/each}
</ul>

<p>Found: {result.length}</p>

{#if result.length}
  {#each result as res, i}
  <li>{i+1} {res}</li>
	{/each}
{/if}