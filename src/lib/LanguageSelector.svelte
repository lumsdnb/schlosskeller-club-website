<script>
	import { language } from '../stores';

	function toggleLanguage() {
		const current = $language.englishSelected;
		$language.englishSelected = !current;
	}
</script>

<div class="bg-black-400 border-4 rounded" on:click={() => toggleLanguage()}>
	{#if $language.englishSelected == false}
		<span class="bg-white text-black">DE</span>
		<span class="bg-black text-white">EN</span>
	{/if}

	{#if $language.englishSelected == true}
		<span class="bg-black text-white">DE</span>
		<span class="bg-white text-black">EN</span>
	{/if}
</div>

<style>
	div {
		color: white;
		font-family: Rubik Mono One;
		width: fit-content;
	}
	span {
		display: inline-block;
		margin: 0rem;
		padding: 0.2rem 0.4rem;
		text-align: center;
		user-select: none;
	}
</style>
