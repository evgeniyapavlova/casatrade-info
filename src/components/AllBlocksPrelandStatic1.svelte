<script>
	import { lang } from '$lib/stores/lang';
	import { base } from '$app/paths';

	import Button from '$common/Button.svelte';
	import Popup from '$common/Popup.svelte';

	import './styles/preland1.scss';
</script>

<section data-lang={$lang}>
	{#each [1, 2, 3, 4] as i}
		<img
			src="{base}/images/shapes/{i}.webp"
			alt="Illustration"
			class="illustration illustration-{i}"
		/>
	{/each}

	<Popup />
	<Button />
</section>
