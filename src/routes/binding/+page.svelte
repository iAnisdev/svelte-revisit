<script lang="ts">
	import BindGroup from '../../component/BindGroup.svelte';
	let name: string = '';
	let age: number = 25;
</script>

<input bind:value={name} placeholder="Enter your name" />
<p>Hello {name}!</p>
<input type="number" bind:value={age} placeholder="Enter your age" />
<p>{name} are {age} years old.</p>

<BindGroup />
