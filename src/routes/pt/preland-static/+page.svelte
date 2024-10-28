<script>
	import { lang } from '$lib/stores/lang';
	import MainPageNew from '$comps/AllBlocksPrelandStatic1.svelte';
	import meta_img from '$lib/images/meta__img__pt.jpg';
	const title = 'Casatrade: uma plataforma de negociação para se sentir em casa';
	const desc = 'Negocie FX, ações, criptomoedas e Opções com 90% de lucratividade';

	$lang = 'pt';
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={desc} />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={desc} />
	<meta property="og:image" content={meta_img} />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={desc} />
	<meta name="twitter:image" content={meta_img} />
</svelte:head>

<MainPageNew lang="pt" />
