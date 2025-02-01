<script lang="ts">
	import { onMount, onDestroy } from 'svelte';
	import type { Map, LatLngExpression } from 'leaflet';
	import { browser } from '$app/environment';
	import depotIcon from '$lib/heart.png';

	interface Marker {
		coordinates: LatLngExpression;
	}

	let markers: Marker[] = [{ coordinates: [48.5836, 8.1472] }];

	const ICON_SIZE = 50;

	let mapElement: HTMLElement;
	let map: Map;

	onMount(async () => {
		if (browser) {
			const leaflet = await import('leaflet');
			map = leaflet.map(mapElement, { scrollWheelZoom: false }).setView([48.583563, 8.1445268], 15);

			leaflet
				.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
					attribution:
						'&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
				})
				.addTo(map);

			const icon = leaflet.icon({
				iconUrl: depotIcon,
				iconSize: [ICON_SIZE, ICON_SIZE]
			});

			markers.forEach((m) => {
				leaflet
					.marker(m.coordinates, { icon })
					.addTo(map)
					.bindPopup(
						`<a href="https://maps.app.goo.gl/rGpZ7awpXJhwmpQq7" target="_blank" rel="noopener noreferrer">Zu Google Maps</a>`
					);
			});
		}
	});

	onDestroy(async () => {
		if (map) {
			map.remove();
		}
	});
</script>

<!-- Workaround for import bug in Leaflet CSS -->
<svelte:head>
	<link
		rel="stylesheet"
		href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
		integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY="
		crossorigin=""
	/>
</svelte:head>

<div class="h-96" bind:this={mapElement}></div>

<style>
</style>
