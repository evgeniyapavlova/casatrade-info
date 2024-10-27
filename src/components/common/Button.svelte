<script>
	import { lang } from '$lib/stores/lang';
	import { linkTraderoom } from '$lib/stores/reg_link';

	const content = {
		en: 'Trade now',
		es: 'Opera ahora',
		pt: 'Negocie agora'
	};
</script>

<a href={$linkTraderoom}>{content[$lang]}</a>

<style>
	a {
		display: inline-block;
		background: linear-gradient(178deg, #2ca249 1.34%, #11421d 98.73%);
		box-shadow:
			0px 68px 47.1px -34px rgba(14, 34, 26, 0.45),
			0px 9.167px 10px 0px #abddea inset;
		color: #f0f3f5;
		text-align: center;
		font-variant-numeric: lining-nums proportional-nums;
		font-family: Inter;
		font-style: normal;
		font-weight: 700;
		line-height: 1;
		width: 264px;
		display: flex;
		height: 60px;
		justify-content: center;
		align-items: center;
		flex-shrink: 0;
		max-width: 100%;
		margin: 0 auto;
		font-size: 19px;
		border-radius: 10px;
		position: relative;
	}
</style>
