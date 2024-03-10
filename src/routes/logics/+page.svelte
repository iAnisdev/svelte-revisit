<script>
	import ColorPicker from '../../component/ColorPicker.svelte';
	let count = 0;

	function increment() {
		count += 1;
	}
</script>

<button on:click={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

{#key count}
	{#if count % 2 === 0}
		<p>Count is even</p>
	{:else if count % 2 === 1}
		<p>Count is odd</p>
	{:else}
		<p>Count is not a number</p>
	{/if}
{/key}

<ColorPicker />
