<script>
	import { onMount } from 'svelte';
	import { getURLParameters } from '$lib/utils/getAffParams';
	import { searchString } from '$lib/stores/affs';
	import { linkTraderoom, linkPWA } from '$lib/stores/reg_link';

	import { lazyLoadBackground } from '$lib/utils/lazyLoadBackground';
	import { scrollToAnchorLinks } from '$lib/utils/scrollToAnchorLinks';

	import '$lib/styles/_constants.scss';
	import '$lib/styles/fonts.css';
	import '$lib/styles/typography.scss';
	import '$lib/styles/buttons.scss';
	import './styles.scss';

	onMount(() => {
		lazyLoadBackground();
		scrollToAnchorLinks();

		$searchString = getURLParameters();
		$linkTraderoom += $searchString;
		$linkPWA += $searchString;
	});
</script>

<div class="app">
	<slot />
</div>

<style>
	.app {
		display: flex;
		flex-direction: column;
		min-height: 100vh;
	}
</style>
