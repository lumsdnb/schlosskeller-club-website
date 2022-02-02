<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import { slide, fly } from 'svelte/transition';
	import '../app.css';
	let y;
	$: console.log(y);
</script>

<svelte:head>
	<title>schlosskeller.club</title>
</svelte:head>

<svelte:window bind:scrollY={y} />

{#if y > 1000}
	<div transition:fly>
		<Header />
	</div>
{/if}

<main>
	<slot />
</main>

<footer>
	<div>
		<span>Poster Gestaltung: <a href="https://www.instagram.com/marianofdeath666">Marian</a></span>
		<br />
		<span>3D & Web Entwicklung: <a href="https://lums.io">Jeremy</a></span> <br />
		<span
			>&copy; 2022 <a href="https://www.schlosskeller-darmstadt.de/">
				Schlosskeller Darmstadt</a
			></span
		>
	</div>
</footer>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 0;
		width: 100%;
		max-width: 1024px;
		box-sizing: border-box;
	}

	footer {
		font-family: 'Rubik Mono One';
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
		background-color: black;
		color: white;
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}
</style>
