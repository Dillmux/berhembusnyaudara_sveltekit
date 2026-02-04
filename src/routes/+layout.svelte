<script>
	import '../app.css';

	import favicon from '$lib/assets/icon.webp';
	// @ts-ignore
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';

	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<Header />
<main class="min-h-screen">
	{@render children()}
</main>
<Footer />
