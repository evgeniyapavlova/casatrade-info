<script>
	import { onMount } from 'svelte';
	import { getURLParameters } from '$lib/utils/getAffParams';
	import { searchString } from '$lib/stores/affs';
	import { linkTraderoom, linkPWA } from '$lib/stores/reg_link';
	import { pageLoaded } from '$lib/stores/pageLoaded';

	import '$lib/styles/fonts.css';
	import './styles.scss';

	onMount(() => {
		$searchString = getURLParameters();
		$linkTraderoom += $searchString;
		$linkPWA += $searchString;
		$pageLoaded = true;

		let vh = window.innerHeight * 0.01;
		document.documentElement.style.setProperty('--vh', `${vh}px`);
	});
</script>

<slot />
