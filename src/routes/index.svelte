<script context="module" lang="ts">
	export const prerender = true;
	import { language } from '../stores';
</script>

<svelte:head>
	<title>Schlosskeller+</title>
</svelte:head>
<div class="scrollContainer">
	<section id="schlosskellerplus">
		<video autoplay muted loop id="myVideo">
			<source src="\video\banner_video.mp4" type="video/mp4" />
			Your browser does not support HTML5 video.
		</video>
		<div class="bannerarcdiv" />

		<div class="welcome">
			<img src="images/skplus.png" id="skplus" alt="" srcset="" />
			Music by
			<ul>
				<li>CHRIS..............................IMPULS</li>
				<li>DAVID........SOULFOOD CLUB</li>
				<li>LAVDIM........LOSTBAHNHOF</li>
				<li>MARIAN..................BOHEMICA</li>
			</ul>
		</div>
		<span class="scrolling-text --left"
			>IMMERSIVE VIRTUAL REALITY EXPERIENCE - BRING YOUR OWN DRINKS</span
		>
		<span class="scrolling-text --right"
			>BIOHAZARD WORLDWIDE STAY AT HOME CYBERSPACE FUTURE PARTY</span
		>
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
					? 'Today we are proud to announce our first event in Darmstadts first virtual event space!'
					: 'Heute freuen wir uns, als erster komplett virtueller Veranstaltungsraum Darmstadts zum ersten Mal die Türen ins Kellergewölbe zu öffnen.'}
			</p>
		</div>
	</section>

	<section id="mitmachen">
		<div class="slide-content flex flex-col lg:flex-col items-center justify-center">
			<h2 class="side-header">
				{$language.englishSelected ? 'Join us' : 'Mitmachen'}
			</h2>
			<p>
				{$language.englishSelected
					? 'We will meet in VRChat. A headset is not required, but makes the experience much more immersive.'
					: 'Wir treffen uns in VRChat. Ein VR Headset ist nicht notwendig, macht das Erlebnis aber immersiver.'}
			</p>
			<br />
			<div class="button-container">
				<div>
					<span class="button-container__counter">1.</span>
					<img class="w-24" src="/images/vrchat-logo.png" alt="" srcset="" />
					<p>
						<a href="https://hello.vrchat.com/">
							{$language.englishSelected ? 'Create account' : 'Account erstellen'}</a
						>
					</p>
				</div>
				<div>
					<span class="button-container__counter">2.</span>
					<p>
						<a href="https://vrchat.com/home/user/usr_933c3cf3-6f8a-44f5-8a87-0f582220a124"
							>{$language.englishSelected
								? 'send us a friend request'
								: 'Kellerkind als Freund hinzufügen'}</a
						>
					</p>
				</div>
				<div>
					<span class="button-container__counter">3.</span>
					<img class="w-14" src="images/invite-icon.png" alt="VrChat invitation icon" srcset="" />
					<p>
						{$language.englishSelected
							? 'You will receive an invite once the event begins'
							: 'Du bekommst zu Beginn der Veranstaltung eine Einladung'}
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
			<details open>
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
							? 'There are different ways to get your own personalized avatar. The easiest would be something like Ready Player Me, which you can create and upload in your browser. A more involved way would be to either find an avatar you like in an avatar world in VRChat, or create one from scratch using 3D software.'
							: 'Es gibt verschiedene Möglichkeiten, um deinen eigenen Avatar zu gestalten. Am einfachsten ist Ready Player Me, wo du einen Avatar im Browser erstellen und hochladen kannst. Du kannst aber auch in VRChat selbst nach Avatar Welten suchen, oder dir einen komplett neuen Avatar in 3D Software gestalten.'}
					</p>
				</div>
			</details>
			<details>
				<summary>
					{$language.englishSelected
						? 'Will there be a limited edition NFT collection?'
						: 'Wird es eine limitierte NFT Kollektion geben?'}
				</summary>
				<div class="faq__content">
					<p>
						{$language.englishSelected
							? 'No, there will not be an NFT collection'
							: 'Nein, es wird keine limitierte NFT Kollektion geben'}
					</p>
				</div>
			</details>

			<div class="button-container">
				<div>
					<img class="w-44" src="/images/discord-logo.png" alt="Discord Logo" />
					<p>
						<a href="https://discord.gg/jxWZvFxry2">
							{$language.englishSelected ? 'join our community' : 'Community beitreten'}
						</a>
					</p>
				</div>
				<div>
					<img class="w-20" src="/images/instagram-logo.png" alt="" srcset="" />
					<p>
						<a href="https://instagram.com/schlosskellerdarmstadt">
							{$language.englishSelected ? 'follow us on insta' : 'Folge uns auf insta'}
						</a>
					</p>
				</div>
			</div>
		</div>
	</section>
	<div style="height:calc(20vh + 80px);scroll-snap-align:end;" />
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
		scroll-snap-stop: normal !important;
		scroll-snap-align: end;
	}

	.slide-content {
		max-width: 90vw;
		filter: drop-shadow(3px 3px 2px black);
	}

	.side-header {
		text-transform: uppercase;
		font-size: 3em;
		position: relative;
		/* left: 4rem;
		top: 5rem; */
		margin: 1rem 0;
		max-width: 50rem;
		line-height: 1.2;
	}

	.smol-header {
		font-size: 2.5rem;
		line-height: 1.2;
	}

	.hover-img:hover {
		transform: scale(1.05);
	}

	.hover-img:active {
		transform: scale(0.95);
	}

	p {
		position: relative;
		max-width: 35rem;
		font-size: 1em;
	}

	section:nth-child(1) {
		max-height: 100vh;
		background-image: url('/images/arc_banner.png');
		z-index: 100;
		position: relative;
	}
	.bannerarc {
		position: absolute;
		z-index: 1000;
		min-height: 100vh;
	}
	.bannerarcdiv {
		background: url('/images/arc_banner.png') no-repeat center;
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
		background-image: url('/images/bild2.webp');
	}
	section:nth-child(3) {
		background-image: url('/images/bild3.webp');
	}
	section:nth-child(4) {
		background-image: url('/images/bild4.webp');
	}
	section:nth-child(5) {
		background-image: url('/images/bild5.webp');
	}
	section:nth-child(6) {
		background-image: url('/images/bild6.webp');
	}

	h1 {
		width: 100%;
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
		background: black no-repeat center;
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
		padding: 0 0 calc(100% * 495 / 2048) 0;
		padding-top: 0px;
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
		padding-top: 95vh;
	}

	.welcome img {
		position: relative;
		height: 40px;
		top: 0;
		display: block;
		z-index: 1000;
		margin-bottom: 32px;
	}

	/* --------------------------- FAQ page -------------------------- */

	summary {
		font-size: 1.25rem;
		font-weight: 600;
		color: var(--accent-color);
		padding: 1rem;
		margin-bottom: 1rem;
		outline: none;
		border-radius: 0.25rem;
		text-align: left;
		cursor: pointer;
		position: relative;
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
		animation: sweep 0.5s ease-in-out;
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
		section {
			background-position: -15rem;
		}
		.button-container {
			flex-direction: column;
		}
	}
</style>
