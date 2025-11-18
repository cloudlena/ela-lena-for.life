<script lang="ts">
	import wedibox from '$lib/images/wedibox.jpg';
	import picdrop from '$lib/images/picdrop.jpg';
</script>

<div class="mx-auto max-w-4xl">
	<header class="my-24 text-center">
		<h1 class="mb-4 text-5xl md:text-8xl">Raphaela & Lena</h1>
		<p class="tagline text-3xl md:text-6xl">20.09.2025</p>
	</header>

	<div class="tagline mb-12 p-6 text-center text-3xl md:text-5xl">
		<p>Vielen Dank ♡ Merci viumau</p>
	</div>

	<div class="flex flex-col items-center justify-between gap-4 text-center lg:flex-row">
		<a
			href="https://my.wedibox.com/rec9a3EKJsJwKm7c"
			target="_blank"
			class="rounded-lg p-8 hover:bg-green-900 hover:text-amber-100 hover:shadow-lg"
		>
			<img src={wedibox} alt="Gäste" class="mb-6 w-full max-w-96 rounded-lg" />
			<p class="text-3xl">Bilder von Euch</p>
		</a>
		<a
			href="https://www.picdrop.com/jujuel/s6WikqK2iJ"
			target="_blank"
			class="rounded-lg p-8 hover:bg-green-900 hover:text-amber-100 hover:shadow-2xl"
		>
			<img src={picdrop} alt="Fotografin" class="mb-6 w-full max-w-96 rounded-lg" />
			<p class="text-3xl">Bilder von der Fotografin</p>
		</a>
	</div>
</div>
