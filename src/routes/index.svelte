<script context="module" lang="ts">
	export const prerender = true;
	import { language } from '../stores';
	import MediaQuery from "./MediaQuery.svelte";
	import CheckIos from './CheckIos.svelte';
</script>
<script>
import { HtmlTag, loop_guard } from "svelte/internal";

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
		<div class="vidarcM">
			
			
			<MediaQuery query="(max-width: 600px)" let:matches>
				{#if matches}
				<CheckIos let:matches>
					{#if matches}
					<img
					id="myVideo"
					alt=""
					autoplay
					loop
					muted
					playsinline
					src="\video\banner_video_iphone.mp4"
					/>
					{/if}
				</CheckIos>
				<CheckIos let:matches>
					{#if !matches}
					<video autoplay muted loop id="myVideo">
						<source src="\video\banner_video_mobile.mp4" type="video/mp4" />
						<source src="\video\banner_video_mobile.webm" type="video/webm" />
					</video>
					{/if}
				</CheckIos>

					{/if}
			</MediaQuery>
			<MediaQuery query="(min-width: 621px)" let:matches>
				{#if matches}
					<video autoplay muted loop id="myVideo">
					<source src="\video\banner_video.mp4" type="video/mp4" />
					<source src="\video\banner_video.webm" type="video/webm" />
					</video>

				{/if}
			</MediaQuery>
			<CheckIos let:matches>
				{#if !matches}
				<div class="bannerarcdiv"></div>
				{/if}
			</CheckIos>


		</div>
		<div class="welcome" style="font-size: {outerWidth > outerHeight? 'calc(16 * 100vw/1/1024)':'calc(18px + 100vw/1/1920)'};">
			<img src="images/skplus.png" style="height: {outerWidth > outerHeight? 'calc(24 * 100vw/1/1024)':'calc(28px + 100vw/1/1920)'};" id="skplus" alt="" srcset="" />
			Music by
			<ul>
				<li>CHRIS..............................IMPULS</li>
				<li>DAVID........SOULFOOD CLUB</li>
				<li>LAVDIM........LOSTBAHNHOF</li>
				<li>MARIAN..................BOHEMICA</li>
			</ul>
		</div>
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
					<p>{$language.englishSelected
							? 'There are different ways to get your own personalized avatar. The easiest would be something like Ready Player Me, which works in the browser. You can also browse avatar worlds in VRChat, or create a custom character using free tools like Vroid Studio.'
							: 'Es gibt verschiedene Möglichkeiten, um deinen eigenen Avatar zu erschaffen. Am einfachsten ist Ready Player Me, wo du einen Avatar im Browser erstellen und hochladen kannst. Du kannst aber auch in VRChat selbst nach Avatar Welten suchen, oder dir einen ganz eigenen in freier 3D Software kreieren.'}
						<a href="https://readyplayer.me">Ready Player Me</a>
						<a href="https://vroid.com/studio">Vroid Studio</a>
					</p>
					<p>
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
	<footer>
		<div>
			<span>
				{$language.englishSelected ? 'Poster design:' : 'Poster Gestaltung:'}
	
				<a href="https://www.instagram.com/marianofdeath666">Marian</a></span
			>
			<br />
			<span>
				{$language.englishSelected ? '3D & Web development:' : '3D & Web Entwicklung:'}
				<a href="https://lums.io">Jeremy</a></span
			> <br />
			<span
				>&copy; 2022 <a href="https://www.schlosskeller-darmstadt.de/">
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
		scroll-snap-stop: normal !important;
		scroll-snap-align: start;
	}

	.slide-content {
		max-width: 90vw;
		filter: drop-shadow(3px 3px 2px black);
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
		background: linear-gradient( 
180deg
, var(--primary-color) 0%, var(--secondary-color) 10.45%, var(--tertiary-color) 51.35%, var(--primary-color) 81.35% );
		max-height: 100vh;
		z-index: 100;
		position: relative;
	}
	.bannerarc {
		position: absolute;
		z-index: 1000;
		min-height: 100vh;
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
	}
	section:nth-child(3) {
		background: url('/images/bild3.webp') center no-repeat;
		background-size: cover;
		padding-top: 64px;
	}
	section:nth-child(4) {
		background: url('/images/bild4.webp') center;
	}
	section:nth-child(5) {
		background: url('/images/bild5.webp') center;
	}
	section:nth-child(6) {
		background: url('/images/bild6.webp') center;
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
		display:flex;
		position: absolute;
		height: 100%;
		width:100%;
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
		background-color: black;
		border: 1px solid white;
	}
	
	details[open] {
		background-color: black;
		border: 1px solid white;
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
		section {
			background-position: -15rem;
		}
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
		zoom: 170%;
		max-height: 100vh;
		overflow: hidden;

		
	}
	.vidarcM video{
		top:-35% !important;
	}
	.vidarcM .bannerarcdiv{
		top:-35% !important;
	}
	.welcome{
		padding-top: 25vh !important;
	}
	}
	@media screen and (max-width: 600px) and (min-height: 700px) {
		.vidarcM {
		zoom: 150%;
		max-height: 100vh;
		overflow: hidden;

		
	}
	.vidarcM video{
		top:-25% !important;
	}
	.vidarcM .bannerarcdiv{
		top:-25% !important;
	}

	}
</style>
