<script lang="ts">
	import Header from "./Header.svelte";
	import Footer from "./Footer.svelte";
	import About from "./About.svelte";
	import Intro from "./Intro.svelte";

	let page: string = "Intro";
	function changePage(newPage: string) {
		page = newPage;
	}
</script>

<Header text="Arsen Mutalapov" on:page={(e) => changePage(e.detail)} />
<main>
	{#if page === "About"}
		<About />
	{:else if page === "Intro"}
		<Intro />
	{/if}
</main>
<Footer />

<style>
	main {
		text-align: center;
		padding: 1em;
		width: 80vw;
		max-width: 240px;
		margin: 5px auto;
		flex-grow: 1;
		border: 3px solid #212f3c;
		border-radius: 40px;
		box-sizing: border-box;
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
			width: 60%;
		}
	}
</style>
