<script>
	import Section from '$lib/components/Section.svelte';
	import ProjectCard from '$lib/components/ProjectCard.svelte';

	const projects = [
		{
			title: 'MFCD',
			description:
				'Full Stack Web Application built with Golang Fiber and MariaDB. Built for a local company to make their website more interactive and seamless. Combining two different websites into one website to make website management more efficient and reduce operational costs.',
			tags: ['Golang', 'Fiber', 'TailwindCSS', 'MariaDB', 'Docker']
		},
		{
			title: 'POR System',
			description:
				"Point of Rental System (Point of Sale System for Rental Business) built with Golang Fiber and MariaDB. Integrated with payment with Midtrans Payment Gateway. <b class='text-md text-brand-light font-semibold'>Ongoing ...</b>",
			tags: ['Golang', 'Fiber', 'MariaDB', 'TailwindCSS'],
			link: 'ongoing'
		},
		{
			title: 'Customer Service Chatbots Integrated with Rental Point of Sale Systems',
			description:
				"LLM-Based AI Agent Model Intelligent System Using n8n for Customer Service Chatbots Integrated with Rental Point of Sale Systems. <b class='text-md text-brand-light font-semibold'>Ongoing ...</b>",
			tags: ['n8n', 'LLM', 'AI Agent', 'Google Gemini', 'API', 'Golang', 'Fiber', 'MariaDB'],
			link: 'ongoing'
		}
	];
</script>

<svelte:head>
	<title>Berhembusnya Udara</title>
	<meta
		name="description"
		content="Portfolio of Berhembusnya Udara - Information Systems Student, Backend Developer, and AI Agent Developer."
	/>
</svelte:head>

<!-- Home / Hero -->
<Section
	id="home"
	class="min-h-screen pt-32 pb-20 justify-center bg-brand-red/20 bg-[url('$lib/assets/hero-bg.svg')] bg-cover bg-center"
>
	<div class="h-96 md:h-128 bg-brand-light bg-[url('$lib/assets/person.webp')] bg-cover bg-center">
		<div class="flex flex-col justify-center px-2 md:px-12 h-full bg-brand-red/35">
			<div class="max-w-4xl animate-fade-in-up space-y-6">
				<h1
					class="text-transparent bg-clip-text bg-linear-to-tr from-brand-black via-brand-black/40 to-brand-red font-antonio font-bold text-6xl md:text-8xl lg:text-9xl leading-none tracking-tighter uppercase"
				>
					Berhembusnya Udara
				</h1>

				<p
					class="px-2 py-1 md:px-4 md:py-2 font-montserrat text-sm md:text-base text-brand-light border-[0.1em] border-brand-light"
				>
					Information Systems Student | Backend Developer Enthusiast (Golang & Fiber) | AI Agent
					Developer with LLM Integration
				</p>

				<div class="flex gap-6">
					<a
						href="#projects"
						class="inline-block px-8 py-1 md:px-10 md:py-2 bg-brand-red text-white font-antonio font-bold text-lg uppercase tracking-widest hover:bg-brand-light hover:text-brand-red transition-all duration-300 shadow-lg hover:shadow-brand-red/30 hover:-translate-y-1"
					>
						My Work
					</a>
					<a
						href="#contacts"
						class="inline-block px-8 py-1 md:px-10 md:py-2 border border-brand-light text-brand-light font-antonio font-bold text-lg uppercase tracking-widest hover:bg-brand-semi hover:border-brand-semi hover:text-brand-black transition-all duration-300 hover:-translate-y-1"
					>
						Contact Me
					</a>
				</div>
			</div>
		</div>
	</div></Section
>

<!-- About -->
<Section id="about" class="bg-brand-black">
	<div class="grid lg:grid-cols-2 gap-16 items-center">
		<div class="order-2 lg:order-1">
			<h2 class="font-antonio font-bold text-5xl md:text-6xl text-white mb-10">
				<span class="text-brand-semi">About</span>
				Me
			</h2>
			<div class="space-y-8 text-stone-400 font-montserrat leading-relaxed text-lg text-justify">
				<p>
					I operate under the alias <span class="text-brand-light font-bold"
						>Berhembusnya Udara</span
					>
					in the digital realm, but in person, I am known as
					<span class="text-brand-light font-bold">Abdi Kuncung</span>. Somehow I wrote
					<span class="text-brand-light font-bold">“tntpl”</span>
					(representing
					<span class="text-brand-light font-bold">Tantipala</span>, Sadewa's pseudonym in his place
					of exile where he worked as a cowherd) on some of my previous works.
				</p>
				<p>
					My journey in technology is driven by a curiosity for how systems work behind the scenes.
					As an <span class="text-white">Information Systems student</span>, I am constantly
					exploring the intersection of business requirements and technical implementation.
				</p>
				<p>
					My core expertise lies in <span class="text-white">Backend Development</span>, where I
					craft efficient, scalable solutions using
					<span class="text-brand-semi font-semibold">Golang</span>
					and <span class="text-brand-semi font-semibold">Fiber</span>. Recently, I have expanded my
					horizons into
					<span class="text-brand-semi font-semibold">AI Agent Development</span>, integrating LLMs
					to build intelligent systems that can perceive, reason, and act.
				</p>
			</div>
		</div>

		<div class="order-1 lg:order-2 relative">
			<div class="aspect-square max-w-md mx-auto relative group">
				<!-- Abstract code visual -->
				<div
					class="absolute inset-0 bg-linear-to-br from-brand-red to-brand-light rounded-2xl transform rotate-3 group-hover:rotate-6 transition-transform duration-500 opacity-20"
				></div>
				<div
					class="absolute inset-0 bg-brand-dark rounded-2xl transform -rotate-3 group-hover:-rotate-6 transition-transform duration-500 opacity-20"
				></div>

				<div
					class="relative h-full w-full bg-black/75 border border-brand-dark/50 rounded-2xl p-8 flex flex-col shadow-2xl overflow-hidden"
				>
					<div class="flex gap-2 mb-6">
						<div class="w-3 h-3 rounded-full bg-brand-red"></div>
						<div class="w-3 h-3 rounded-full bg-brand-semi"></div>
						<div class="w-3 h-3 rounded-full bg-brand-light"></div>
					</div>

					<code class="font-mono text-sm md:text-base text-stone-300 overflow-hidden">
						<span class="text-green-500">package</span> main<br /><br />
						<span class="text-green-500">import</span> (<br />
						&nbsp;&nbsp;"github.com/gofiber/fiber/v2"<br />
						)<br /><br />
						<span class="text-green-500">func</span>
						<span class="text-brand-light">main</span>() &#123;<br />
						&nbsp;&nbsp;app := fiber.New()<br /><br />
						&nbsp;&nbsp;app.Get(<span class="text-brand-light">"/"</span>,
						<span class="text-green-500">func</span>(c *fiber.Ctx) error &#123;<br />
						&nbsp;&nbsp;&nbsp;&nbsp;<span class="text-green-500">return</span>
						c.SendString(<span class="text-brand-light">"Hello, World!"</span>)<br />
						&nbsp;&nbsp;&#125;)<br /><br />
						&nbsp;&nbsp;app.Listen(<span class="text-brand-light">":3000"</span>)<br />
						&#125;
					</code>
				</div>
			</div>
		</div>
	</div>
</Section>

<!-- Projects -->
<Section id="projects" class="bg-linear-to-br from-brand-black to-brand-red/20">
	<div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6">
		<div>
			<p
				class="text-brand-light text-right md:text-left font-montserrat font-bold tracking-widest uppercase mb-2"
			>
				Portfolio
			</p>
			<h2 class="font-antonio font-bold text-5xl md:text-6xl text-white">
				Selected <span class="text-brand-semi">Projects</span>
			</h2>
		</div>
		<a
			href="https://github.com/Dillmux/"
			target="_blank"
			rel="noopener noreferrer"
			class="text-stone-400 hover:text-brand-light flex items-center gap-2 group transition-colors"
		>
			<span class="uppercase tracking-widest text-sm font-bold">View All Github</span>
			<svg
				xmlns="http://www.w3.org/2000/svg"
				class="w-5 h-5 transform group-hover:translate-x-1 transition-transform"
				fill="none"
				viewBox="0 0 24 24"
				stroke="currentColor"
				><path
					stroke-linecap="round"
					stroke-linejoin="round"
					stroke-width="2"
					d="M17 8l4 4m0 0l-4 4m4-4H3"
				/></svg
			>
		</a>
	</div>

	<div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
		{#each projects as project}
			<ProjectCard {...project} />
		{/each}
	</div>
</Section>

<!-- Contact -->
<Section id="contacts">
	<div
		class="max-w-4xl mx-auto text-center bg-brand-dark border border-brand-dark/30 p-12 md:p-20 rounded-3xl relative overflow-hidden backdrop-blur-sm"
	>
		<div class="relative z-10">
			<h2 class="font-antonio font-bold text-5xl md:text-6xl text-white mb-8">
				<span class="text-transparent bg-clip-text bg-linear-to-br from-brand-semi/75 to-brand-red"
					>Connect</span
				> to Me
			</h2>
			<p class="text-stone-300 font-montserrat text-lg md:text-xl mb-12 max-w-2xl mx-auto">
				I am currently open for opportunities in Backend and Web Development. Of course, I am also
				open to opportunities to design small-scale (as a micro service) to medium-scale AI agent
				workflows. Have a project in mind or want to discuss the future of tech?
			</p>

			<div class="flex flex-col sm:flex-row gap-6 justify-center">
				<a
					href="mailto:abdillah.nafima@yahoo.com"
					target="_blank"
					class="px-8 py-1 md:px-10 md:py-2 bg-brand-light text-brand-black font-antonio font-bold text-xl uppercase tracking-widest hover:bg-white transition-colors duration-300 shadow-xl shadow-brand-light/10"
				>
					Say Hello
				</a>
				<a
					href="https://linkedin.com/in/berhembusnyaudara"
					target="_blank"
					class="px-8 py-1 md:px-10 md:py-2 border-2 border-stone-600 text-stone-300 font-antonio font-bold text-xl uppercase tracking-widest hover:border-brand-semi hover:text-brand-semi transition-colors duration-300"
				>
					LinkedIn
				</a>
			</div>
		</div>

		<!-- background glow -->
		<div
			class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[120%] h-[120%] bg-radial-gradient from-brand-red/10 to-transparent z-0 pointer-events-none"
		></div>
	</div>
</Section>
