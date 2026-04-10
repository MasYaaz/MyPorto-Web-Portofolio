<script>
	import { ui } from '$lib/stores/UIStates.svelte';
	import { ArrowDown } from 'lucide-svelte';
	import Image from './Home/Image.svelte';
</script>

<!-- Section 1 -->
<section
	class="relative flex min-h-screen w-full items-center justify-center overflow-hidden bg-[url('/images/back.webp')] bg-cover bg-center px-6 lg:px-16"
	id="section_1"
>
	<!-- Overlay dengan gradien yang lebih halus -->
	<div
		class="absolute inset-0 bg-linear-to-b from-secondary/70 via-secondary/90 to-secondary dark:from-primary/80 dark:via-primary/95 dark:to-primary"
	></div>

	<div
		class="z-10 container mx-auto flex w-full max-w-7xl flex-col items-center justify-between gap-12 lg:flex-row lg:pt-0"
	>
		<!-- Sisi Kiri: Tulisan -->
		<div
			class="order-1 flex h-full flex-1 flex-col items-center gap-4 text-center transition-all duration-700 lg:items-start lg:gap-6 lg:text-left"
		>
			<div class="text-primary dark:text-secondary">
				<h1 class="font-primary text-6xl leading-none font-black uppercase lg:text-8xl">Hello</h1>
				<p class="font-primary text-4xl font-bold lg:text-5xl">Everybody!</p>
			</div>

			<p
				class="font-secondary max-w-md text-lg font-medium tracking-wide text-primary/90 lg:text-xl dark:text-secondary/90"
			>
				I am <span class="font-bold text-primary dark:text-white">Aflah Mahdi Yazdi</span>,
				<span class="mt-2 block text-sm leading-relaxed font-normal normal-case md:text-lg">
					An emerging Full-Stack Developer building high-performance web apps with
					<span
						class="underline decoration-primary decoration-2 underline-offset-4 dark:decoration-secondary"
						>SvelteKit</span
					>,
					<span
						class="underline decoration-primary decoration-2 underline-offset-4 dark:decoration-secondary"
						>Rust</span
					>, and intelligent AI automation.
				</span>
			</p>
			<div class="flex flex-col items-center lg:items-start">
				<!-- Animasi bounce pada icon panah -->
				<div class="mt-4 hidden animate-bounce lg:block">
					<ArrowDown size={48} class="text-primary dark:text-secondary" />
				</div>
			</div>

			<button
				onclick={() => ui.scrollToSection('section_2')}
				aria-label="Next Button"
				class="font-secondary bg-primary px-8 py-4 text-lg font-black text-secondary uppercase shadow-[0_10px_20px_rgba(0,0,0,0.2)] transition-all duration-300 hover:-translate-y-1 hover:cursor-pointer hover:bg-primary/90 active:scale-95 lg:text-2xl dark:bg-secondary dark:text-primary dark:hover:bg-white"
			>
				My Profil
			</button>
		</div>

		<!-- Sisi Kanan: Call to Action -->
		<div
			class="order-3 flex flex-1 flex-col items-center gap-6 text-center lg:items-end lg:justify-center lg:text-right"
		></div>
	</div>
</section>
