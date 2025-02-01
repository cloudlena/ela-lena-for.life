<script lang="ts">
	import '../app.css';
	import Menu from './Menu.svelte';

	let { children } = $props();
</script>

<div>
	{@render children()}

	<Menu />
</div>
