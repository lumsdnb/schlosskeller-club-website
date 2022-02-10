<script lang="ts">
	import { page } from '$app/stores';
	import logo from '$lib/header/sk-logo.svg';
	import LanguageSelector from '$lib/LanguageSelector.svelte';
	import { language } from '../../stores';
</script>

<header>
	<!-- Primary Meta Tags -->
	<title>Schlosskeller+</title>
	<meta name="title" content="Schlosskeller+" />
	<meta
		name="description"
		content="BIOHAZARD WORLDWIDE STAY AT HOME CYBERSPACE FUTURE PARTY - IMMERSIVE VIRTUAL REALITY EXPERIENCE - BRING YOUR OWN DRINKS "
	/>

	<!-- Open Graph / Facebook -->
	<meta property="og:type" content="website" />
	<meta property="og:url" content="https://schlosskeller.club/" />
	<meta property="og:title" content="Schlosskeller+" />
	<meta
		property="og:description"
		content="BIOHAZARD WORLDWIDE STAY AT HOME CYBERSPACE FUTURE PARTY - IMMERSIVE VIRTUAL REALITY EXPERIENCE - BRING YOUR OWN DRINKS "
	/>
	<meta property="og:image" content="" />

	<!-- Twitter -->
	<meta property="twitter:card" content="summary_large_image" />
	<meta property="twitter:url" content="https://schlosskeller.club/" />
	<meta property="twitter:title" content="Schlosskeller+" />
	<meta
		property="twitter:description"
		content="BIOHAZARD WORLDWIDE STAY AT HOME CYBERSPACE FUTURE PARTY - IMMERSIVE VIRTUAL REALITY EXPERIENCE - BRING YOUR OWN DRINKS "
	/>
	<meta property="twitter:image" content="" />
	<div class="corner">
		<a href="#schlosskellerplus">
			<!-- <img src={logo} alt="Schlosskeller+" /> -->
			<img src="/logo.png" id="header-image" alt="" srcset="" />
		</a>
	</div>

	<nav>
		<ul class="flex">
			<li>
				<!-- <a href="#schlosskellerplus">Schlosskeller+</a> -->
			</li>
			<li>
				<a href="#mitmachen">
					{$language.englishSelected ? 'Join' : 'Mitmachen'}
				</a>
			</li>
			<li><a href="#faq">FAQ</a></li>
		</ul>
		<div class="langsel">
			<LanguageSelector />
		</div>
	</nav>
</header>

<style>
	.langsel {
		height: fit-content;
		display: flex;
		justify-content: center;
		align-items: center;
		margin: 1rem;
		border: 1px solid white;
	}
	header {
		display: flex;
		justify-content: space-between;
		height: 6vh;
		min-height: 4rem;
		position: fixed;
		top: 0;
		width: 100%;
		z-index: 2;
		background: rgb(2, 0, 36);
		background: linear-gradient(
			180deg,
			rgba(0, 0, 0, 0.9) 0%,
			rgba(0, 0, 0, 0.9) 61%,
			rgba(0, 0, 0, 0) 100%
		);
		overflow: hidden;
	}

	.corner {
		width: 9em;
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
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 100%;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
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

	#header-image {
		height: auto;
		width: auto;
		float: left;
		object-fit: cover;
	}
</style>
