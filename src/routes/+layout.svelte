<script lang="ts">
	import Menu from './Menu.svelte';
	import '../app.css';

	let { children } = $props();
</script>

<div>
	<main>
		{@render children()}
	</main>

	<Menu />
</div>
