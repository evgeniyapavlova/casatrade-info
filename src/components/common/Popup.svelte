<script>
	import { lang } from '$lib/stores/lang';
	import { linkTraderoom } from '$lib/stores/reg_link';
	import { pageLoaded } from '$lib/stores/pageLoaded';

	const content = {
		en: {
			now: 'now',
			popup_text: '1,500$ has been credited to your account from CasaTrade'
		},
		es: {
			now: 'ahora',
			popup_text: 'CasaTrade ha acreditado 1500$ a su cuenta.'
		},
		pt: {
			now: 'agora',
			popup_text: 'R$ 8500 foram creditados em sua conta da CasaTrade'
		}
	};
</script>

<a id="popup" href={$linkTraderoom} class:visible={$pageLoaded}>
	<div class="popup-head">
		<div class="popup-head-left">
			<div class="popup-icon">
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="14"
					height="12"
					viewBox="0 0 14 12"
					fill="none"
				>
					<path
						d="M0.0952148 3.93705L6.81891 0.351074L13.5426 3.93705V12.0055H0.0952148V3.93705Z"
						fill="#5B95EE"
					/>
					<rect x="5.92236" y="3.93713" width="1.79299" height="5.82721" fill="white" />
					<rect x="2.78516" y="6.17834" width="1.79299" height="3.58597" fill="white" />
					<rect x="9.06006" y="6.17834" width="1.79299" height="3.58597" fill="white" />
				</svg>
			</div>
			Casatrade
		</div>
		<div class="popup-head-right">{content[$lang].now}</div>
	</div>
	<div class="popup-content">{content[$lang].popup_text}</div>
</a>

<style>
	#popup {
		border-radius: 12px;
		padding: 10px 16px 10px 10px;
		position: fixed;
		top: 34px;
		max-width: 320px;
		width: 90%;
		margin: 0 auto;
		font-family: 'SF Pro Display';
		font-weight: 400;
		line-height: normal;
		transform: translate3d(0px, -60px, 0px);
		transition:
			transform 0.5s ease-out,
			opacity 0.4s ease-out;
		transform-style: preserve-3d;
		opacity: 0;
		transition-delay: 0.8s;
	}

	#popup.visible {
		opacity: 1;
		transform: none;
	}

	.popup-icon {
		width: 20px;
		height: 20px;
		border-radius: 5px;
		background-color: #292929;
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.popup-head {
		color: rgba(0, 0, 0, 0.2);
		font-size: 12px;
		letter-spacing: -0.12px;
		display: flex;
		align-items: center;
		justify-content: space-between;
		margin-bottom: 8px;
	}

	.popup-head-left {
		display: flex;
		align-items: center;
		justify-content: flex-start;
		gap: 7px;
		text-transform: uppercase;
	}

	.popup-content {
		color: #000;

		font-size: 14px;
		font-weight: 400;
		letter-spacing: -0.14px;
		max-width: 85%;
	}

	/* @media screen and (min-width: 1080px) {
		#popup {
			border-radius: 32px;
			max-width: 880px;
			padding: 28px 44px 28px 28px;
			top: 160px;
		}

		.popup-head {
			font-size: 33px;
			letter-spacing: -0.3px;
			margin-bottom: 22px;
		}

		.popup-content {
			font-size: 39px;
			letter-spacing: -0.4px;
		}

		.popup-icon {
			height: 56px;
			width: 56px;
			border-radius: 12px;
		}

		svg {
			width: 38px;
			height: auto;
		}

		.popup-head-left {
			gap: 19px;
		}
	} */
</style>
