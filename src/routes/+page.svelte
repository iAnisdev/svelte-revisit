<script lang="ts">
	import AddNumbers from '../component/AddNumbers.svelte';
	import Increment from '../component/Increment.svelte';
	import UserCard from '../component/UserCard.svelte';

	let name: string = 'World';
	let paragraph: string = 'This is a paragraph';
	let htmlParagraph: string = '<strong>This is a paragraph</strong>';

	let user: User = {
		name: 'Sd',
		age: 29,
		email: 'sd@gmail.com'
	};
</script>

<h1>Hello {name}!</h1>
<hr />

<p>{paragraph}</p>
<p>{htmlParagraph}</p>
<p>{@html htmlParagraph}</p>

<hr />

<Increment />

<hr />

<AddNumbers />
<AddNumbers numbToAdd={1} />
<AddNumbers numbToAdd={2} />

<hr />

<UserCard />
<UserCard {...user} />

<hr />

<style>
	p {
		color: goldenrod;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
</style>
