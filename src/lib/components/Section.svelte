<script>
	let { id, class: className = '', children } = $props();
</script>

<section
	{id}
	class="py-20 md:py-28 min-h-[50vh] flex flex-col justify-center relative overflow-hidden {className}"
>
	<!-- Background gradient accent -->
	<div
		class="absolute top-0 left-0 w-full h-px bg-linear-to-r from-transparent via-brand-dark/20 to-transparent"
	></div>

	<div class="container mx-auto px-6 relative z-10 h-full">
		{@render children()}
	</div>
</section>
