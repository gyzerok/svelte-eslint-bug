<script lang="ts">
	import type { SvelteSet } from 'svelte/reactivity';

	type Props = {
		set: SvelteSet<number>;
	};

	let { set = $bindable() }: Props = $props();
</script>

{#each set as value, i (i)}
	<button onclick={() => set.delete(value)}>
		{value}
	</button>
{/each}
