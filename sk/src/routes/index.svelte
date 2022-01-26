<script context="module" lang="ts">
	export const prerender = true;
</script>

<svelte:head>
	<title>schlosskeller.club</title>
</svelte:head>

<section>
	<h1>
		SEITE IST NOCH NICHT FERTIG PLS NOCH MIT LEUTEN TEILEN DANKE LG
		<div class="welcome">
			<picture>
				<source srcset="svelte-welcome.webp" type="image/webp" />
				<img src="svelte-welcome.png" alt="Welcome" />
			</picture>
			Lineup
			<ul>
				<li>Chris (Impuls)</li>
				<li>David (Soulfood Club)</li>
				<li>Marian (Bohemica)</li>
				<li>Lavdim (deep shit</li>
			</ul>
		</div>
	</h1>
</section>

<section>
	<p>Aus unbekannten Gründen hat der Schlosskeller immer noch zu.</p>
	<p>Wir haben Anfang 2020 mit Live Streams experimentiert, konnten damit aber nie die gleiche Cluberfahrung bieten.</p>
	<p>Heute freuen wir uns, als erster digitalisierter Club Darmstadts mit euch zusammen zu feiern.</p>
</section>

<section id="mitmachen">
	<h2>Mitmachen</h2>
	<p>Wir treffen uns in VRChat. Ein VR Headset ist nicht notwendig, macht das Erlebnis aber immersiver.</p> 
	<p>Um zu uns zu finden, muss dich ein Kellerkind zu Beginn der Veranstaltung einladen. Du findest uns auf unserer Discord Community, wo weitere Infos zur Veranstaltung bekannt gegeben werden.</p>
	<p>Die Teilnehmerzahl ist limitiert. Früh kommen lohnt sich!</p>
	<div class="button-container">
		<div>VRChat Account erstellen</div>
		<div>Discord Community beitreten</div>
	</div>
</section>

<section id="regeln">
	<div><p>18+</p></div>
	<div><p>Du darfst dich bei uns frei ausdrücken. Achte aber bitte darauf, dass dein avatar nicht zu komplex ist. Dein Avatar ist zu groß, wenn du nicht mehr durch die Tür passt.</p></div>
	<div><p>BYOB - Wir können Getränke noch nicht über Datenleitungen streamen, sobald das geht wird Chris sicherlich auch wieder die Zapfanlage anmachen.</p></div>
</section>

<section>
	<h3>bis bald</h3>
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
	}

	@media screen and (max-width: 20rem){
		section{
			background-position: -15rem;
		}
	}

	p{
		max-width: 20rem;
	}

	section:nth-child(1) {
		background-image: url("/images/bild1.png");
	}
	section:nth-child(2) {
		background-image: url("/images/bild2.png");
	}
	section:nth-child(3) {
		background-image: url("/images/bild3.png");
	}
	section:nth-child(4) {
		background-image: url("/images/bild4.png");
	}
	section:nth-child(5) {
		background-image: url("/images/bild5.png");
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
		width: 20%;
		height: 20%;
		top: 0;
		display: block;
	}
</style>
