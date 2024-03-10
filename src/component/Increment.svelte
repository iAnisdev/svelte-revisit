<script lang="ts">
	let count: number = 0;
	$: double = count * 2;

	$: {
		console.log('count updated' , count);
		console.log('double updated');
	}

	function increment() {
		count += 1;
	}
</script>

<button on:click={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

<p>Double is {double}</p>
