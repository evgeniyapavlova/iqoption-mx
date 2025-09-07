<script>
	import { onMount } from 'svelte';
	import { base } from '$app/paths';
	import meta__img from '$lib/images/meta__img.jpg';
	import './styles.css';

	import { iframe_params } from '../lib/constants/reg_link';

	function updateLinks() {
		iframe_params.set(window.location.search);
	}

	onMount(() => {
		updateLinks();
	});

	const title = 'IQ Option: Entrar, Qué Es, Cómo Funciona Broker en México';
	const desc =
		'IQ Option México: plataforma de trading para CFDs, criptomonedas y Forex. Depósitos mínimos, registro fácil y operación inmediata.';
</script>

<svelte:head>
	<title>{title}</title>
	<meta name="description" content={desc} />
	<meta property="og:title" content={title} />
	<meta property="og:description" content={desc} />
	<meta property="og:image" content={meta__img} />

	<meta name="twitter:site" content="iqoption.mx" />
	<meta name="twitter:card" content="summary_large_image" />
	<meta name="twitter:title" content={title} />
	<meta name="twitter:description" content={desc} />
	<meta name="twitter:image" content={meta__img} />
	<link rel="canonical" href="https://iqoption.mx" />
	<link
		rel="preload"
		as="image"
		href="{base}/images/bg_intro.webp"
		type="image/webp"
		fetchpriority="high"
	/>
</svelte:head>

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
