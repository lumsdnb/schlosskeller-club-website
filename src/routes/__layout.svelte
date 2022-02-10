<script lang="ts">
	import Header from '$lib/header/Header.svelte';
	import { slide, fly } from 'svelte/transition';
	import '../app.css';
	import { language } from '../stores';
	let y;

	//$: console.log(y);
</script>

<svelte:head>
	<title>schlosskeller.club</title>
</svelte:head>

<!-- <svelte:window bind:scrollY={y} /> -->

<!-- {#if y > 500} -->
<div transition:fly>
	<Header />
</div>
<!-- {/if} -->

<main>
	<slot />
</main>

<style>
	main {
		flex: 1;
		display: flex;
		flex-direction: column;
		padding: 0;
		width: 100%;
		max-width: 100%;
		box-sizing: border-box;
		scroll-snap-type: y proximity;
	}

	footer {
		font-family: Gruppo;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		padding: 40px;
		background-color: black;
		color: white;
		height: 20vh;
		z-index: -1;
		font-size: 1rem;
		height: calc(20vh + 80px);
		margin-top: calc(-20vh - 80px);
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
