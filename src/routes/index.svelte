<script context="module" lang="ts">
	export const prerender = true;
	import { language } from '../stores';
	import MediaQuery from './MediaQuery.svelte';
	import CheckIos from './CheckIos.svelte';
</script>

<script>
	import { HtmlTag, loop_guard } from 'svelte/internal';

	$: outerWidth = 0;
	$: innerWidth = 0;
	$: outerHeight = 0;
	$: innerHeight = 0;
</script>

<svelte:window bind:innerWidth bind:outerWidth bind:innerHeight bind:outerHeight />

<svelte:head>
	<title>Schlosskeller+</title>
</svelte:head>

<div class="scrollContainer">
	<section id="schlosskellerplus">
		<img src="/images/museumsposter.webp">
	</section>

	<section>
		<div class="slide-content flex flex-col lg:flex-row">
			<p class="m-5">
				{$language.englishSelected
					? 'Due to unknown reasons, Schlosskeller is still closed.'
					: 'Aus unbekannten Gründen hat der Schlosskeller immer noch zu.'}
			</p>

			<p class="m-5">
				{$language.englishSelected
					? 'In 2020 we experimented with live streams, but could never achieve a level of immersion comparable with a real club experience.'
					: 'Wir haben Anfang 2020 mit Live Streams experimentiert, konnten damit aber nie die gleiche Cluberfahrung bieten.'}
			</p>
			<br />
			<p class="m-5">
				{$language.englishSelected
					? 'Today we are proud to announce our first ~CYBERSPACE~ party in Darmstadts first virtual event space!'
					: 'Heute freuen wir uns, als erster komplett virtueller Veranstaltungsraum Darmstadts unser Kellergewölbe im ~CYBERSPACE~ zu öffnen.'}
			</p>
		</div>
	</section>

	<section id="mitmachen">
		<div class="slide-content flex flex-col lg:flex-col items-center justify-center">
			<h2 class="side-header">
				{$language.englishSelected ? 'how to join' : 'Mitmachen'}
			</h2>
			<p>
				{$language.englishSelected
					? 'We will meet in VRChat on June 15th at 7PM GMT+1. A headset is not required, but makes the experience much more immersive.'
					: 'Wir treffen uns am 15. Juni um 19 Uhr in VRChat. Ein Headset ist nicht notwendig, macht das Erlebnis aber immersiver.'}
			</p>
			<br />
			<div class="button-container">
				<div>
					<span class="button-container__counter">1.</span>
					<img class="w-24" src="/images/vrchat-logo.png" alt="" srcset="" />
					<p>
						<a href="https://hello.vrchat.com/" target="_blank">
							{$language.englishSelected ? 'Create account' : 'Account erstellen'}</a
						>
					</p>
				</div>
				<div>
					<span class="button-container__counter">2.</span>
					<p>
						<a
							href="https://vrchat.com/home/user/usr_933c3cf3-6f8a-44f5-8a87-0f582220a124"
							target="_blank"
							>{$language.englishSelected
								? 'Add lumsdnb as a friend'
								: 'lumsdnb als Freund hinzufügen'}</a
						>
					</p>
				</div>
				<div>
					<span class="button-container__counter">3.</span>
					<img class="w-14" src="images/orb.png" alt="VrChat invitation icon" srcset="" />
					<p>
						{$language.englishSelected
							? 'Once our status turns blue, you will be able to join the party!'
							: 'Sobald unser Status blau wird, ist die Party eröffnet!'}
					</p>
				</div>
			</div>
			<p class="mb-10">
				{$language.englishSelected
					? 'Depending on network conditions, the maximum number of participants is limited between 50 to 80 people. Come early!'
					: 'Die Teilnehmerzahl ist je nach Netzwerkauslastung auf 50-80 Personen limitert. Früh kommen lohnt sich!'}
			</p>
		</div>
	</section>

	<section id="regeln">
		<div class="flex sm:flex-row flex-col slide-content">
			<div class="m-2 flex flex-col justify-center items-center">
				<h2 class="smol-header">18+</h2>
				<p class="text-center">
					{$language.englishSelected
						? 'No minors! We will attempt to verify your age at the door'
						: 'Alterskontrollen am Eingang'}
				</p>
			</div>
			<div class="m-8">
				<h2 class="smol-header">Avatar Limits</h2>
				<p class="text-right">
					{$language.englishSelected
						? 'You are free to express yourself however you like, but please be mindful of VRChats avatar performance limits. If you get stuck at the door, your avatar is probably too big.'
						: 'Du darfst dich bei uns frei ausdrücken. Achte aber bitte darauf, dass dein Avatar nicht zu komplex ist. Dein Avatar ist zu groß, wenn du nicht mehr durch die Tür passt.'}
				</p>
			</div>
		</div>
	</section>
	<section id="byod">
		<div class="slide-content">
			<h2 class="side-header">Bring your own drinks</h2>
			<p>
				{$language.englishSelected
					? 'As of now, we are unable to stream drinks over the network. We will let you know once we figure out how to do that.'
					: 'Wir können Getränke leider noch nicht über Datenleitungen streamen. Sobald das geht, wird Chris sicherlich auch wieder die Zapfanlage in Betrieb nehmen.'}
			</p>
		</div>
	</section>

	<section id="faq">
		<div class="flex sm:flex-col items-center flex-col slide-content">
			<h2 class="side-header">FAQ</h2>

			<div class="faqsection">
				<details>
					<summary
						>{$language.englishSelected
							? 'Do I need a VR headset?'
							: 'Brauche ich eine VR Brille?'}</summary
					>
					<div class="faq__content">
						<p>
							{$language.englishSelected
								? 'No, VRChat, despite the name, can also be played on a regular computer.'
								: 'Nein, VRChat kann auch auf dem Computer gespielt werden.'}
						</p>
					</div>
				</details>
				<details>
					<summary>
						{$language.englishSelected
							? 'How do I create a custom avatar?'
							: 'Wie erstelle ich einen eigenen Avatar?'}
					</summary>
					<div class="faq__content">
						<p>
							{$language.englishSelected
								? 'There are different ways to get your own personalized avatar. The easiest would be something like Ready Player Me, which works in the browser. You can also browse avatar worlds in VRChat, or create a custom character using free tools like Vroid Studio.'
								: 'Es gibt verschiedene Möglichkeiten, um deinen eigenen Avatar zu erschaffen. Am einfachsten ist Ready Player Me, wo du einen Avatar im Browser erstellen und hochladen kannst. Du kannst aber auch in VRChat selbst nach Avatar Welten suchen, oder dir einen ganz eigenen in freier 3D Software kreieren.'}
							<br /> <br />
							<a class="pt-2 pb-2" href="https://readyplayer.me">Ready Player Me</a> <br />
							<a href="https://vroid.com/studio">Vroid Studio</a> <br />
						</p>
						<p class="pt-5">
							{$language.englishSelected
								? 'Feel free to ask for help on our Discord server, we will do our best to help you get your creation online.'
								: 'Solltest du Fragen zur Avatar Erstellung haben, können wir dir auf unserem Discord Server helfen.'}
						</p>
					</div>
				</details>
				<details>
					<summary>
						{$language.englishSelected
							? 'Will there be a limited NFT collection?'
							: 'Wird es eine limitierte NFT Kollektion geben?'}
					</summary>
					<div class="faq__content">
						<p>
							{$language.englishSelected
								? 'No, there will be no limited NFT collection.'
								: 'Nein, es wird keine limitierte NFT Kollektion geben.'}
						</p>
					</div>
				</details>
			</div>

			<div class="button-container">
				<div>
					<img class="w-44" src="/images/discord-logo.png" alt="Discord Logo" />
					<p>
						<a href="https://discord.gg/jxWZvFxry2" target="_blank">
							{$language.englishSelected ? 'join our community' : 'Community beitreten'}
						</a>
					</p>
				</div>
				<div>
					<img class="w-20" src="/images/instagram-logo.png" alt="" srcset="" />
					<p>
						<a href="https://instagram.com/schlosskellerdarmstadt" target="_blank">
							{$language.englishSelected ? 'follow us on Instagram' : 'Folge uns auf Instagram'}
						</a>
					</p>
				</div>
			</div>
		</div>
	</section>
	<footer>
		<div>
			<span>
				{$language.englishSelected ? 'Poster design:' : 'Poster Gestaltung:'}

				<a href="https://www.instagram.com/marianofdeath666" target="_blank">Marian</a></span
			>
			<br />
			<span>
				{$language.englishSelected ? '3D & Web development:' : '3D & Web Entwicklung:'}
				<a href="https://lums.io" target="_blank">Jeremy</a> &
				<a
					href="https://www.linkedin.com/in/angel-oris-manu-pumahualca-perez-6908ba207/"
					target="_blank">Manú</a
				></span
			> <br />
			<span
				>&copy; 2022 <a href="https://www.schlosskeller-darmstadt.de/" target="_blank">
					Schlosskeller Darmstadt</a
				></span
			>
		</div>
	</footer>
</div>

<style>
	.scrollContainer {
		overflow: auto;
		width: 100%;
		height: 100vh;
		scroll-snap-type: y proximity;
		scroll-behavior: smooth !important;
	}
	section {
		max-width: 100%;
		min-height: 100vh;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		background-repeat: no-repeat;
		background-size: cover;
		position: relative;
		scroll-snap-align: start;
	}

	.slide-content {
		max-width: 90vw;
		filter: drop-shadow(3px 5px 1px black);
	}

	.side-header {
		text-transform: uppercase;
		font-size: 2.5em;
		position: relative;
		/* left: 4rem;
		top: 5rem; */
		margin: 1rem 0;
		max-width: 50rem;
		line-height: 1.2;
		padding-top: 3rem;
	}

	.smol-header {
		font-size: 2.5rem;
		line-height: 1.2;
	}

	p {
		position: relative;
		max-width: 35rem;
		font-size: 1em;
		filter: drop-shadow(2px 2px 0px black) !important;
	}

	section:nth-child(1) {
		background-color: #64ad87;
		background-size: contain;
		max-height: 100vh;
		z-index: 100;
		position: relative;
		overflow: hidden;
	}

	.bannerarcdiv {
		background: url('/images/arc_banner.webp') no-repeat center;
		background-size: cover;
		position: absolute;
		z-index: 100;
		min-height: 100vh;
		max-height: 100vh;
		width: 100%;
	}
	#myVideo {
		position: absolute;
		right: 0;
		top: 0;
		min-width: 100%;
		min-height: 100vh;
		max-height: 100vh;
		object-fit: cover;
		z-index: 10;
	}
	section:nth-child(2) {
		background: url('/images/bild2.webp') center;
		background-size: cover;
	}
	section:nth-child(3) {
		background: url('/images/bild3.webp') center no-repeat;
		background-size: cover;
		padding-top: 64px;
	}
	section:nth-child(4) {
		background: url('/images/bild4.webp') center no-repeat;
		background-size: cover;
	}
	section:nth-child(5) {
		background: url('/images/bild5.webp') center no-repeat;
		background-size: cover;
	}
	section:nth-child(6) {
		background: url('/images/bild6.webp') center no-repeat;
		background-size: cover;
	}

	.button-container {
		display: flex;
		flex-direction: row;
		font-size: 2rem;
		margin: 1.5rem;
		font-family: Gruppo;
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
		background-color: rgba(0, 0, 0, 0.3);
		background-attachment: fixed;
		background-size: cover;
		color: white;
		border: 2px solid white;
		margin: 0.5rem;
		max-width: 18rem;
	}

	.button-container p {
		line-height: 0.9;
	}

	.button-container > div:hover {
		transform: scale(1.05);
		transition: all 70ms ease-in-out;
	}

	.welcome {
		position: relative;
		width: 100%;
		z-index: 10;
		text-align: center;
		top: 48%;
		font-family: 'Gismonda FG', sans-serif;
		color: white;
		filter: drop-shadow(2px 2px 2px black);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding-top: 30vh;
	}

	.welcome img {
		position: relative;
		top: 0;
		display: block;
		z-index: 1000;
		margin-bottom: 32px;
	}

	.vidarcM {
		display: flex;
		position: absolute;
		height: 100%;
		width: 100%;
	}
	/*---Footer---*/
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
	}

	footer a {
		font-weight: bold;
	}

	@media (min-width: 480px) {
		footer {
			padding: 40px 0;
		}
	}

	/* --------------------------- FAQ page -------------------------- */

	.faqsection {
		width: 80vw;
		max-width: 35rem;
		font-size: 1.5rem;
	}

	summary {
		font-size: 1.8rem;
		font-weight: 600;
		color: var(--accent-color);
		padding: 1rem;
		margin-bottom: 1rem;
		outline: none;
		border-radius: 0.25rem;
		text-align: left;
		cursor: pointer;
		position: relative;
		background-color: rgba(0, 0, 0, 0.3);
	}

	details[open] {
		padding: 1.2rem;
		background-color: rgba(0, 0, 0, 0.3);
	}

	details > summary::after {
		position: absolute;
		content: '+';
		right: 20px;
	}
	details[open] > summary::after {
		position: absolute;
		content: '-';
		right: 20px;
	}
	details > summary::-webkit-details-marker {
		display: none;
	}

	details[open] summary ~ * {
		animation: sweep 0.2s ease-in-out;
	}
	@keyframes sweep {
		0% {
			opacity: 0;
			margin-left: -10px;
		}
		100% {
			opacity: 1;
			margin-left: 0px;
		}
	}

	@media screen and (max-width: 45rem) {
		.button-container {
			flex-direction: column;
		}
	}
	@media screen and (max-width: 600px) {
		.bannerarcdiv {
			background: url('/images/arc_banner_mobile.webp') no-repeat center;
			background-size: cover;
			position: absolute;
			z-index: 100;
			min-height: 100vh;
			max-height: 100vh;
			width: 100%;
		}
		.vidarcM {
			transform: translate(0, 40vh) scale(1.5);
			max-height: 100vh;
			overflow: visible;
		}
		section:nth-child(2) {
			background: url('/images/bild2-mobil.webp') center;
		}
		section:nth-child(3) {
			background: url('/images/bild3-mobil.webp') center no-repeat;
			background-size: cover;
			padding-top: 0;
		}
		section:nth-child(4) {
			background: url('/images/bild4-mobil.webp') center;
		}
		section:nth-child(5) {
			background: url('/images/bild5-mobil.webp') center;
		}
		section:nth-child(6) {
			background: url('/images/bild6-mobil.webp') center;
		}

		.vidarcM video {
			top: -35% !important;
		}
		.vidarcM img {
			top: -27% !important;
		}
		.vidarcM .bannerarcdiv {
			top: -35% !important;
		}
		.welcome {
			padding-top: 25vh !important;
		}
	}
	@media screen and (max-width: 600px) and (min-height: 700px) {
		.vidarcM {
			transform: translate(0, 40vh) scale(1.4);
			max-height: 100vh;
			overflow: visible;
		}
		.vidarcM video {
			top: -25% !important;
		}
		.vidarcM img {
			top: -22% !important;
		}
		.vidarcM .bannerarcdiv {
			top: -25% !important;
		}
	}
</style>
