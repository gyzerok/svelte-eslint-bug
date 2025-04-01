<script lang="ts">
	import { SvelteSet } from 'svelte/reactivity';
	import Bug3 from './Bug3.svelte';

	let set = $state(new SvelteSet<number>([]));

	$effect(() => {
		console.log(set);
	});
</script>

<Bug3 bind:set />
