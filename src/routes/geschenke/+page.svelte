<script lang="ts">
	import japan from './japan.webp';

	interface Gift {
		name: string;
		description: string;
		image: string;
	}

	const gifts: Gift[] = [
		{
			name: 'Reise nach Japan',
			description: 'Wir planen schon länger eine Reise nach Japan',
			image: japan
		}
	];
</script>

<div class="mx-auto max-w-4xl">
	<div class="mb-24 mt-12 text-center">
		<h1 class="mb-4 text-4xl md:text-6xl">Geschenke</h1>
		<p class="text-2xl md:text-4xl">Diese Sachen wünschen wir uns schon lange</p>
	</div>

	<div class="mb-24 grid gap-6 p-6 text-center text-3xl md:grid-cols-3 md:text-5xl">
		{#each gifts as gift}
			<div class="max-w-sm overflow-hidden rounded bg-white shadow-lg">
				<img class="mb-6 h-40 w-full object-cover" src={gift.image} alt={gift.name} />
				<div class="px-6">
					<div class="mb-4 min-h-14 text-xl font-bold">{gift.name}</div>
					<p class="mb-4 text-base text-gray-700">
						{gift.description}
					</p>
				</div>
				<div class="flex px-6 pb-2">
					<a
						class="mb-2 mr-2 inline-block w-full rounded-full bg-green-900 px-3 py-1 text-sm font-semibold text-gray-700 text-white hover:bg-gray-400 hover:bg-green-800"
						href="/danke"
						target="_blank"
						rel="noopener noreferrer">Schenken</a
					>
				</div>
			</div>
		{/each}
	</div>
</div>
