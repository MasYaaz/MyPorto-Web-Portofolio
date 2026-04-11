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
			<Image />
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
				class="font-secondary w-full max-w-md bg-primary p-3 text-lg font-medium tracking-wide lg:bg-transparent lg:pt-12 lg:text-xl lg:text-primary dark:lg:text-secondary"
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
