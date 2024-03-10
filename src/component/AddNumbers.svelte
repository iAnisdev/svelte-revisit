<script lang="ts">
	let numbers: Array<number> = [1, 2, 3, 4];
	export let numbToAdd: number = 1;
	function addNumber() {
		numbers = [...numbers, numbers[numbers.length - 1] + numbToAdd];
	}

	$: sum = numbers.reduce((total, currentNumber) => total + currentNumber, 0);
</script>

<p>{numbers.join(' + ')} = {sum}</p>

<button on:click={addNumber}> Add a number </button>
