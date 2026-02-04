<script>
	let y = $state(0);
	let isMenuOpen = $state(false);

	const links = [
		{ name: 'Home', href: '#home' },
		{ name: 'About', href: '#about' },
		{ name: 'Projects', href: '#projects' },
		{ name: 'Contacts', href: '#contacts' }
	];

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}

	import icon from '$lib/assets/icon.webp';
</script>

<svelte:window bind:scrollY={y} />

<header
	class="fixed w-full top-0 z-50 transition-all duration-300 {y > 20
		? 'bg-brand-black/90 shadow-xl backdrop-blur-md py-3'
		: 'bg-transparent py-6'}"
>
	<div
		class="container mx-auto px-6 flex flex-row-reverse md:flex-row justify-between items-center"
	>
		<a
			href="/"
			class="font-antonio font-bold text-xl md:text-2xl text-brand-light tracking-wide uppercase"
		>
			<!-- Berhembusnya Udara -->
			<img src={icon} alt="" height="64px" width="64px" />
		</a>

		<!-- Desktop Nav -->
		<nav class="hidden md:flex gap-8 items-center">
			{#each links as link}
				<a
					href={link.href}
					class="text-stone-300 hover:text-brand-light transition-colors font-montserrat font-medium text-sm tracking-widest uppercase relative group"
				>
					{link.name}
					<span
						class="absolute -bottom-1 left-0 w-0 h-0.5 bg-brand-light transition-all group-hover:w-full"
					></span>
				</a>
			{/each}
		</nav>

		<!-- Mobile Menu Button -->
		<button class="md:hidden text-brand-light p-2" onclick={toggleMenu} aria-label="Toggle menu">
			{#if isMenuOpen}
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"><path d="M18 6 6 18" /><path d="m6 6 12 12" /></svg
				>
			{:else}
				<svg
					xmlns="http://www.w3.org/2000/svg"
					width="24"
					height="24"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
					stroke-linecap="round"
					stroke-linejoin="round"
					><line x1="4" x2="20" y1="12" y2="12" /><line x1="4" x2="20" y1="6" y2="6" /><line
						x1="4"
						x2="20"
						y1="18"
						y2="18"
					/></svg
				>
			{/if}
		</button>
	</div>

	<!-- Mobile Nav -->
	{#if isMenuOpen}
		<div
			class="md:hidden absolute top-full left-0 w-full bg-brand-black/95 backdrop-blur-xl border-t border-brand-dark/30 shadow-2xl"
		>
			<nav class="flex flex-col py-6 px-6">
				{#each links as link}
					<a
						href={link.href}
						class="text-stone-300 hover:text-brand-light py-4 border-b border-brand-dark/20 text-center font-montserrat font-medium tracking-widest uppercase"
						onclick={() => (isMenuOpen = false)}
					>
						{link.name}
					</a>
				{/each}
			</nav>
		</div>
	{/if}
</header>
