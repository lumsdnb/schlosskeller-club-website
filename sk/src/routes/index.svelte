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
	<p>enter the partyverse</p>
	<Countdown />
</section>

<section class="fullpanel">
	<p>enter the partyverse</p>
</section>

<section>
	<p>
		Seit einiger Zeit ist der Schlosskeller geschlossen, und Streams haben uns nach ner Weile
		gelangweilt.
	</p>
	<p>Wir freuen uns, euch jetzt wieder virtuell in den Keller einzuladen</p>
</section>

<style>
	section {
		width: 100vw;
		height: 95vh;
	}
	section:nth-child(odd) {
		background-color: rgb(204, 204, 204);
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
