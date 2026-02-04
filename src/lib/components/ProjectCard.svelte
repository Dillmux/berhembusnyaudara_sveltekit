<script>
	let { title, description, tags = [], link = '#projects' } = $props();

	// @ts-ignore
	function disablelink(event) {
		event.preventDefault();
	}
</script>

<a
	href={link === 'ongoing' ? '#projects' : link}
	target="_blank"
	rel="noopener noreferrer"
	class="group block h-full bg-linear-to-br from-brand-dark/10 to-transparent border border-brand-dark/30 hover:border-brand-semi/50 p-6 md:p-8 rounded-xl transition-all duration-300 hover:bg-brand-dark/20 hover:-translate-y-2 hover:shadow-2xl hover:shadow-brand-red/5"
	onclick={link === '#projects' || link === 'ongoing' ? disablelink : undefined}
>
	<div class="flex flex-col h-full">
		<div class="flex justify-between items-start gap-1 mb-4">
			<h3
				class="w-6/7 font-antonio font-bold text-2xl text-white group-hover:text-brand-light transition-colors"
			>
				{title}
			</h3>
			<div class="w-1/7 flex justify-end">
				{#if link === '#projects'}{:else if link === 'ongoing'}
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="w-6 h-6 text-stone-600 group-hover:text-brand-light transition-colors transform group-hover:translate-x-1 group-hover:-translate-y-1"
						height="24px"
						viewBox="0 -960 960 960"
						width="24px"
						fill="currentColor"
						><path
							d="M160-120q-33 0-56.5-23.5T80-200v-200q0-33 23.5-56.5T160-480h200q0 50 35 85t85 35q50 0 85-35t35-85h200q33 0 56.5 23.5T880-400v200q0 33-23.5 56.5T800-120H160Zm0-80h640v-200H664q-25 55-74.5 87.5T480-280q-60 0-109.5-32.5T296-400H160v200Zm544-328-56-56 142-142 56 56-142 142Zm-448 0L114-670l56-56 142 142-56 56Zm184-112v-200h80v200h-80ZM160-200h640-640Z"
						/></svg
					>
				{:else}
					<svg
						xmlns="http://www.w3.org/2000/svg"
						class="w-6 h-6 text-stone-600 group-hover:text-brand-light transition-colors transform group-hover:translate-x-1 group-hover:-translate-y-1"
						fill="none"
						viewBox="0 0 24 24"
						stroke="currentColor"
						><path
							stroke-linecap="round"
							stroke-linejoin="round"
							stroke-width="2"
							d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14"
						/></svg
					>
				{/if}
			</div>
		</div>

		<p
			class="text-stone-400 font-montserrat text-sm leading-relaxed mb-6 group-hover:text-stone-300 transition-colors grow"
		>
			{@html description}
		</p>

		<div
			class="flex flex-wrap gap-2 pt-4 border-t border-brand-dark/20 group-hover:border-brand-dark/40 transition-colors"
		>
			{#each tags as tag}
				<span
					class="text-xs font-montserrat font-semibold px-3 py-1 rounded-full bg-brand-black/50 text-brand-semi border border-brand-dark/30 group-hover:border-brand-semi/30 group-hover:text-brand-light transition-colors"
				>
					{tag}
				</span>
			{/each}
		</div>
	</div>
</a>
