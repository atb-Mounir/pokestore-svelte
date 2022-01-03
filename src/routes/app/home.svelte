<script>
    import {pokemon} from "../../stores/pokestore";
    import PokemonCard from "../../components/pokemonCard.svelte";
    console.log($pokemon);
</script>
<svelte:head>
    <title>Sveltes Kit Pokdex</title>
</svelte:head>

<h1 class="text-4xl text-center my-8 uppercase">Svelte Kit Pokedex</h1>

<!--
  This example requires Tailwind CSS v2.0+ 
  
  This example requires some changes to your config:
  
  ```
  // tailwind.config.js
  module.exports = {
    // ...
    plugins: [
      // ...
      require('@tailwindcss/aspect-ratio'),
    ],
  }
  ```
-->
<div class="bg-white">
    <div class="max-w-2xl mx-auto py-16 px-4 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">
      <h2 class="text-2xl font-extrabold tracking-tight text-gray-900">Customers also purchased</h2>
  
      <div class="mt-6 grid grid-cols-1 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">

        {#each $pokemon as pokeman}
        <PokemonCard pokeman={pokeman} />
    {/each}
        <!-- More products... -->
      </div>
    </div>
  </div>
  



