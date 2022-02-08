<script>
	import { language } from '../stores';

	function toggleLanguage() {
		const current = $language.englishSelected;
		$language.englishSelected = !current;
	}
</script>

<div on:click={() => toggleLanguage()}>
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
		font-family: Gruppo;
		width: 100%;
		height: 50%;
		user-select: none;
		display: flex;
		justify-content: center;
		align-items: center;
		padding: 0;
		margin: 0;
	}
	span {
		/* padding: 0.2rem 0.4rem; */
		text-align: center;
		font-size: 1.5rem;
	}
</style>
