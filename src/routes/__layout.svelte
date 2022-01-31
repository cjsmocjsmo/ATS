<script context="module">
	import Header from '$lib/header/Header.svelte';
	import FootComp from '$lib/comps/footericonscomp.svelte';
	import AddrComp from '$lib/comps/addresscomp.svelte';
	import { Styles, Image } from 'sveltestrap';
	import '../app.css';
</script>

<Styles />

<Header />

<main>
	<slot />
</main>

<footer>
	<a href="tel:360 516 8933"><h1>360 516 8933</h1></a>
	<AddrComp />
	<FootComp />
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 1rem;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}

	a {
		text-decoration: none;
	}

	h1 {
		color: white;
	}

	footer {
		background-color: blue;
	}
</style>
