<script context="module" lang="ts">
	export const prerender = true;
</script>

<script lang="ts">
	import Countdown from '$lib/Countdown.svelte';
</script>

<svelte:head>
	<title>Home</title>
</svelte:head>

<section>
	<h1>
		<div class="welcome">
			<picture>
				<source srcset="svelte-welcome.webp" type="image/webp" />
				<img src="svelte-welcome.png" alt="Welcome" />
			</picture>
		</div>
	</h1>
</section>

<section class="fullpanel">
	<p>enter the partyverse</p>
	<Countdown />
</section>

<section>
	<p>
		Seit einiger Zeit ist der Schlosskeller geschlossen, und Streams haben uns nach ner Weile
		gelangweilt.
	</p>
	<p>Wir freuen uns, euch jetzt wieder virtuell in den Keller einzuladen</p>
</section>

<section>
	<h2>WIE NEHME ICH TEIL?</h2>
	<ol>
		<li>VRChat auf Steam installieren und einen VRChat Account erstellen</li>
		<li>Schlosskeller User als Freund hinzufuegen</li>
		<li>Am Tag des Events VRChat oeffnen und auf einen EInladungslink warten</li>
	</ol>
</section>

<section>
	<h3>bis bald</h3>
</section>

<style>
	section {
		width: 100vw;
		height: 95vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		font-size: 2rem;
	}
	section:nth-child(even) {
		background-color: rgb(53, 53, 53);
	}

	h1 {
		width: 100%;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
