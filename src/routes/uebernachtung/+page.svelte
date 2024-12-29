<script lang="ts">
	import rebstock from './rebstock.jpg';
	import schusterjunge from './schusterjunge.avif';

	interface Stay {
		name: string;
		description: string;
		image: string;
		link: string;
		address: string;
		position: number[];
	}

	const stays: Stay[] = [
		{
			name: 'Landgasthof Rebstock',
			description:
				'Wir nehmen uns gerne Zeit für Sie und wünschen Ihnen eine genussvolle Zeit hier bei uns im Rebstock in Furschenbach.',
			image: rebstock,
			link: 'https://www.landgasthofrebstock.de/',
			address: 'Dorfstraße 1, 77883 Ottenhöfen im Schwarzwald',
			position: [48.5795887, 8.1330446]
		},
		{
			name: 'Schusterjunge',
			description: 'Ferien & Business Apartments für Urlauber:innen und Geschäftsreisende.',
			image: schusterjunge,
			link: 'https://www.schusterjunge-aparthotel.de/',
			address: 'Im Winkel 1, 77887 Sasbachwalden',
			position: [48.6183827, 8.1224028]
		}
	];
</script>

<div class="mx-auto max-w-4xl">
	<div class="mb-24 text-center">
		<h1 class="mb-4 text-4xl md:text-6xl">Übernachtungsmöglichkeiten</h1>
		<p class="text-3xl md:text-5xl">in der Umgebung</p>
	</div>

	<p class="text-center text-4xl">Map</p>

	<div class="mb-24 grid gap-6 p-6 text-center text-3xl md:grid-cols-3 md:text-5xl">
		{#each stays as stay}
			<div class="max-w-sm overflow-hidden rounded shadow-lg">
				<img class="w-full" src={stay.image} alt={stay.name} />
				<div class="px-6 py-4">
					<div class="mb-2 text-xl font-bold">{stay.name}</div>
					<p class="text-base text-gray-700">
						{stay.description}
					</p>
				</div>
				<div class="px-6 pb-2 pt-4">
					<a
						class="mb-2 mr-2 inline-block rounded-full bg-gray-300 px-3 py-1 text-sm font-semibold text-gray-700 hover:bg-gray-400"
						href={stay.link}
						target="_blank"
						rel="noopener noreferrer">Zur Website</a
					>
				</div>
			</div>
		{/each}
	</div>
</div>
