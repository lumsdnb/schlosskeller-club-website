<script context="module" lang="ts">
	export const prerender = true;
	import { language } from '../stores';
</script>

<svelte:head>
	<title>schlosskeller.club</title>
</svelte:head>

<section id="schlosskellerplus">
	<h1>
		SEITE IST NOCH NICHT FERTIG PLS NOCH NICHT MIT LEUTEN TEILEN DANKE LG
		<div class="welcome">
			Lineup
			<ul>
				<li>Chris (Impuls)</li>
				<li>David (Soulfood Club)</li>
				<li>Marian (Bohemica)</li>
				<li>Lavdim (lostbahnhof)</li>
			</ul>
		</div>
	</h1>
</section>

<section>
	<p>
		{$language.englishSelected
			? 'Aus unbekannten Gründen hat der Schlosskeller immer noch zu.'
			: ''}
	</p>

	<p>
		Wir haben Anfang 2020 mit Live Streams experimentiert, konnten damit aber nie die gleiche
		Cluberfahrung bieten.
	</p>
	<p>
		Heute freuen wir uns, als erster komplett virtueller Veranstaltungsraum Darmstadts zum ersten
		Mal die Türen ins Kellergewölbe zu öffnen.
	</p>
</section>

<section id="mitmachen">
	<h2 class="side-header">Mitmachen</h2>
	<p>
		Wir treffen uns in VRChat. Ein VR Headset ist nicht notwendig, macht das Erlebnis aber
		immersiver.
	</p>
	<br />
	<div class="button-container">
		<div>
			<span class="button-container__counter">1.</span>
			<img class="w-24" src="/images/vrchat-logo.png" alt="" srcset="" />
			<a href="https://hello.vrchat.com/">Account erstellen</a>
		</div>
		<div>
			<span class="button-container__counter">2.</span>
			Kellerkind als
			<a href="https://vrchat.com/home/user/usr_933c3cf3-6f8a-44f5-8a87-0f582220a124"
				>Freund hinzufügen</a
			>
		</div>
		<div>
			<span class="button-container__counter">3.</span>
			<img class="w-24" src="images/invite-icon.png" alt="VrChat invitation icon" srcset="" /> Zu Beginn
			der Veranstaltung wirst du eingeladen
		</div>
	</div>
	<p>
		Die Teilnehmerzahl ist je nach Netzwerkauslastung auf 50-80 Personen limitert. Früh kommen lohnt
		sich!
	</p>
</section>

<section id="regeln">
	<div class="flex">
		<div class="m-2">
			<h2 class="smol-header">18+</h2>
			<p>Alterskontrollen am Eingang</p>
		</div>
		<div class="m-8">
			<h2 class="smol-header">Avatar Limits</h2>
			<p>
				Du darfst dich bei uns frei ausdrücken. Achte aber bitte darauf, dass dein Avatar nicht zu
				komplex ist. <br /> Dein Avatar ist zu groß, wenn du nicht mehr durch die Tür passt.
			</p>
		</div>
	</div>
</section>
<section id="byod">
	<h2 class="side-header">Bring your own drinks</h2>
	<p>
		Wir können Getränke leider noch nicht über Datenleitungen streamen. Sobald das geht, wird Chris
		sicherlich auch wieder die Zapfanlage anmachen.
	</p>
</section>

<section>
	<h3 class="max-w-md">
		Weitere infos und Ankündigungen zu dieser und weiteren veranstaltungen findest du hier
	</h3>

	<div class="flex m-8 text-white">
		<a href="https://discord.gg/jxWZvFxry2"
			><img class="w-44 hover-img" src="/images/discord-logo.png" alt="Discord Logo" /></a
		>
		<a href="https://instagram.com/schlosskellerdarmstadt"
			><img class="w-20 hover-img" src="/images/instagram-logo.png" alt="" srcset="" /></a
		>
	</div>
	<h3 class="max-w-md ">Nein, wir werden keine NFTs verkaufen</h3>
</section>

<style>
	section {
		width: 100vw;
		height: 100vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-repeat: no-repeat;
		background-size: cover;
		position: relative;
	}

	.side-header {
		text-transform: uppercase;
		font-size: 3rem;
		position: absolute;
		left: 4rem;
		top: 5rem;
	}

	.hover-img:hover {
		transform: scale(1.05);
	}

	.hover-img:active {
		transform: scale(0.95);
	}

	p {
		max-width: 24rem;
	}

	section:nth-child(1) {
		background-image: url('/images/bild1.png');
	}
	section:nth-child(2) {
		background-image: url('/images/bild2.png');
	}
	section:nth-child(3) {
		background-image: url('/images/bild3.png');
	}
	section:nth-child(4) {
		background-image: url('/images/bild4.png');
	}
	section:nth-child(5) {
		background-image: url('/images/bild5.png');
	}
	section:nth-child(6) {
		background-image: url('/images/bild6.png');
	}

	h1 {
		width: 100%;
	}

	.button-container {
		display: flex;
		flex-direction: row;
		margin: 2rem;
		font-family: Rubik Mono One;
	}
	.button-container__counter {
		position: absolute;
		top: 0.6rem;
		left: 0.6rem;
	}

	.button-container > div {
		position: relative;
		display: flex;
		flex-direction: column;
		text-align: center;
		align-items: center;
		justify-content: center;
		padding: 2rem;
		background-color: black;
		color: white;
		border: 2px solid white;
		margin: 0.5rem;
		max-width: 18rem;
	}

	.welcome {
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 20%;
		height: 20%;
		top: 0;
		display: block;
	}
	@media screen and (max-width: 45rem) {
		section {
			background-position: -15rem;
		}
		.button-container {
			flex-direction: column;
		}
	}
</style>
