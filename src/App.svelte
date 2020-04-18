<script>
	import About from "./components/About.svelte"
	import Other from "./components/Other.svelte"
	import Person from "./components/Person.svelte"
	export let name;
	export let lastName;
	//export let age;
	let svelteLogo = "https://arepa.s3.amazonaws.com/svelte-logo.png";

	const data = {
		name: 'Abraham',
		lastName: 'Lora',
		age: 19,
	}

</script>

<style>

	:global(body) {
		background-color: #f2eee2;
		color: #0084f6;
	}

	:global(:root) {
		--theme-color: purple;
	}

	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	main img {
		width: 30%;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>

<main>
	<h1>¡Hello {name} {lastName}!</h1>
	<About />
	<Other anotherText="Hola!" />
	<Other />
	<Person {...data} />

	<img src={svelteLogo} alt="Svelte"/>
</main>