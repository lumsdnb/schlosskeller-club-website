<script lang="ts">
	import { page } from '$app/stores';
	import logo from './sk-logo.svg';
	import LanguageSelector from '$lib/LanguageSelector.svelte';
	export let englishSelected = false;
</script>

<header>
	<div class="corner">
		<a href="/">
			<img src={logo} alt="Schlosskeller+" />
		</a>
	</div>

	<nav>
		<ul>
			<li>
				<a href="#schlosskellerplus">Schlosskeller+</a>
			</li>
			<li><a href="#mitmachen">Mitmachen</a></li>
			<li><a href="#regeln">Regeln</a></li>
			<li><a href="#faq">FAQ</a></li>
		</ul>
	</nav>

	<div class="corner">
		<LanguageSelector />
	</div>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
		height: 5vh;
		position: fixed;
		top: 0;
		width: 100%;
		z-index: 1;
		background-color: black;
	}

	.corner {
		width: 9em;
		height: 6em;
		position: relative;
		left: 1em;
		top: 0.2em;
	}

	.corner a {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		height: 100%;
	}

	/* .corner img {
		width: 2em;
		height: 2em;
		object-fit: contain;
	} */

	nav {
		display: flex;
		justify-content: center;
		--background: rgba(10, 10, 10, 0.7);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
	}

	li {
		position: relative;
		height: 100%;
		display: flex;
		justify-content: center;
		align-items: center;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 700;
		font-size: 0.8rem;
		text-transform: uppercase;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--accent-color);
	}
</style>
