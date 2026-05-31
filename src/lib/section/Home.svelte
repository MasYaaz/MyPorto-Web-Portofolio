<script>
	import Back1 from '$lib/component/Background/Back1.svelte';
	import { ui } from '$lib/stores/UIStates.svelte';
	import Image from './Home/Image.svelte';
</script>

<!-- Section 1 -->
<section
	class="relative flex min-h-screen w-full items-center justify-center overflow-hidden"
	id="section_1"
>
	<!-- Overlay dengan gradien yang lebih halus -->
	<Back1 />
	<div
		class="z-10 container mx-auto flex w-full max-w-7xl flex-col items-center justify-center gap-6 p-10 pt-20"
	>
		<div
			class="flex h-full w-screen flex-col items-center text-center text-secondary transition-all duration-700 lg:w-fit dark:text-secondary"
		>
			<div class="relative flex items-center justify-center">
				<svg
					class="absolute top-2 left-28 z-0 h-12 w-12 animate-bounce text-orange opacity-80"
					viewBox="0 0 24 24"
					style="animation-duration: 3.5s;"
					fill="currentColor"
				>
					<path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z" />
				</svg>

				<svg
					class="absolute top-18 right-20 z-0 h-8 w-8 animate-pulse text-primary opacity-60 dark:text-secondary"
					viewBox="0 0 24 24"
					fill="currentColor"
				>
					<path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z" />
				</svg>

				<svg
					class="absolute right-6 bottom-5 z-0 h-14 w-14 animate-bounce text-aqua opacity-80"
					viewBox="0 0 24 24"
					fill="currentColor"
					style="animation-duration: 3.5s;"
				>
					<path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z" />
				</svg>

				<svg
					class="absolute bottom-6 left-8 z-0 h-6 w-6 text-primary opacity-60 dark:text-secondary"
					viewBox="0 0 24 24"
					fill="currentColor"
				>
					<path d="M12 0L14.6 9.4L24 12L14.6 14.6L12 24L9.4 14.6L0 12L9.4 9.4L12 0Z" />
				</svg>

				<Image />
			</div>
			<h1
				class="w-full bg-orange mask-intersect py-4 font-primary text-6xl leading-none font-black uppercase lg:-mt-3 lg:w-fit lg:-rotate-1 lg:mask-[radial-gradient(circle_12px_at_0_0,transparent_99%,black_100%),radial-gradient(circle_12px_at_100%_0,transparent_99%,black_100%),radial-gradient(circle_12px_at_100%_100%,transparent_99%,black_100%),radial-gradient(circle_12px_at_0_100%,transparent_99%,black_100%)] lg:p-4 lg:pb-6 lg:text-8xl"
			>
				Welcome
			</h1>
			<p
				class="w-full bg-aqua mask-intersect py-3 font-primary text-4xl font-bold lg:w-fit lg:-rotate-1 lg:mask-[radial-gradient(circle_12px_at_0_0,transparent_99%,black_100%),radial-gradient(circle_12px_at_100%_0,transparent_99%,black_100%),radial-gradient(circle_12px_at_100%_100%,transparent_99%,black_100%),radial-gradient(circle_12px_at_0_100%,transparent_99%,black_100%)] lg:p-4 lg:pb-6 lg:text-5xl"
			>
				to my web porto!
			</p>
			<p
				class="font-secondary w-full bg-primary p-3 text-lg font-medium tracking-wide lg:w-fit lg:bg-transparent lg:pt-12 lg:text-xl lg:text-primary dark:bg-secondary dark:text-primary dark:lg:bg-transparent dark:lg:text-secondary"
			>
				Come on to know more about me
			</p>
		</div>

		<button
			onclick={() => ui.scrollToSection('section_2')}
			aria-label="Next Button"
			class="font-secondary scallop-box relative bg-primary px-10 py-5 text-lg font-black text-secondary uppercase shadow-[0_10px_20px_rgba(0,0,0,0.2)] transition-all duration-300 hover:-translate-y-1 hover:cursor-pointer hover:bg-primary/95 active:scale-95 lg:text-2xl dark:bg-secondary dark:text-primary dark:hover:bg-white"
		>
			My Profil
		</button>
	</div>
</section>
