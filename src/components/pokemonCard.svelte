<script>
	export let pokeman;

	function remove() {
		pokeman.splice(pokeman.id, pokeman.id);
	}
</script>

<button on:click={remove(pokeman.id)}>remove</button>
<div class="group relative">
	<div class="mt-4 flex justify-between">
		<div>
			<h3 class="text-sm text-gray-700">
				<a href="./{pokeman.id}">
					<span aria-hidden="true" class="absolute inset-0" />
					{pokeman.id}. {pokeman.name}
				</a>
			</h3>
			<!-- <p class="mt-1 text-sm text-gray-500">Black</p> -->
		</div>

		<!-- <p class="text-sm font-medium text-gray-900">$35</p> -->
	</div>
	<div
		class="w-full min-h-80 bg-gray-200 aspect-w-1 aspect-h-1 rounded-md overflow-hidden group-hover:opacity-75 lg:h-80 lg:aspect-none"
	>
		<img
			src={pokeman.image}
			alt={pokeman.name}
			class="w-full h-full object-center object-cover lg:w-full lg:h-full"
		/>
	</div>
</div>
<!-- <a class="bg-gray-200" href="{`/pokeman/${pokeman.id}`}">
    <img src={pokeman.image} alt={pokeman.name}>
    <h2>{pokeman.id}. {pokeman.name}</h2>
</a> -->
