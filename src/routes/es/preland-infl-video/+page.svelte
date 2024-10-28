<script>
	import { lang } from '$lib/stores/lang';
	import MainPageNew from '$comps/AllBlocksPrelandStatic3_2.svelte';
	import meta_img from '$lib/images/meta__img__3_2__es.jpg';
	const title = 'Casatrade — una plataforma de trading que es cómo estar en casa';
	const desc = 'Opera con FX, valores, criptomonedas, y opciones con 90% de rentabilidad';

	$lang = 'es';
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

<MainPageNew lang="es" />
