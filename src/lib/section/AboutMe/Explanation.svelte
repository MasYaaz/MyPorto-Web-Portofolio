<script>
	import profil from '$lib/images/profil-2.webp';
</script>

<div class="flex w-full max-w-7xl flex-col gap-6 px-2 pt-20 xl:flex-row">
	<img
		src={profil}
		alt="Foto Personal"
		class="h-full w-full object-contain px-2 shadow-xl lg:m-12 lg:rotate-2"
	/>
	<div class="flex transform flex-col items-center gap-6 lg:my-12">
		<div class="grid w-full grid-cols-1 gap-4 px-2 md:grid-cols-2 md:gap-6 lg:px-0">
			<div
				class="scallop-box group col-span-1 flex flex-col justify-center bg-primary px-6 py-8 text-center transition-all duration-300 hover:scale-[1.02] hover:rotate-0 md:col-span-2 md:px-10 lg:rotate-1 dark:bg-secondary"
			>
				<p
					class="font-secondary text-[10px] font-bold tracking-widest text-secondary uppercase opacity-80 md:text-base dark:text-primary"
				>
					My Name
				</p>
				<h2
					class="font-primary text-3xl font-black tracking-tighter text-secondary uppercase sm:text-4xl 2xl:text-6xl dark:text-primary"
				>
					Aflah Mahdi Yazdi
				</h2>
			</div>

			<div
				class="scallop-box group flex flex-col items-center justify-center bg-orange p-6 text-secondary transition-all duration-300 hover:scale-[1.02] hover:rotate-0 md:-rotate-2 lg:-rotate-1"
			>
				<p
					class="font-secondary text-[10px] font-bold tracking-widest uppercase opacity-70 md:text-xs"
				>
					From
				</p>
				<p class="font-primary text-2xl font-black uppercase 2xl:text-4xl">Indonesia</p>
			</div>

			<div
				class="scallop-box group flex flex-col items-center justify-center bg-aqua p-6 text-secondary transition-all duration-300 hover:scale-[1.02] hover:rotate-0 md:rotate-2 lg:rotate-1 dark:bg-secondary dark:text-primary"
			>
				<p
					class="font-secondary text-[10px] font-bold tracking-widest uppercase opacity-70 md:text-xs"
				>
					Base
				</p>
				<p class="font-primary text-2xl font-black uppercase 2xl:text-4xl">Surabaya</p>
			</div>
		</div>
		<div
			class="scallop-box relative bg-orange p-8 text-secondary shadow-sm transition-all duration-700 ease-out dark:text-secondary"
		>
			<span
				class="absolute top-4 left-4 -translate-x-2 -translate-y-3 font-serif text-7xl opacity-20 select-none md:text-9xl"
			>
				“
			</span>

			<p
				class="relative z-10 text-center font-display text-sm leading-relaxed md:text-base lg:text-lg"
			>
				As an enthusiastic
				<span class="font-bold text-primary dark:text-secondary">Full-Stack Developer</span>, I am
				deeply passionate about building fast and reliable web applications using
				<span class="italic">Svelte</span> and
				<span class="italic">Rust</span>. While I consider myself a continuous learner in this
				evolving field, I have already gained hands-on experience integrating
				<span class="font-semibold text-primary dark:text-secondary">Supabase</span>
				for back-end logic and exploring local AI ecosystems with
				<span class="italic">Ollama</span>.
				<br /><br />
				Currently, I am focusing on developing
				<span class="font-semibold text-primary dark:text-secondary">WhatsApp chatbots</span>
				and complex web interfaces that bridge the gap between functionality and design. My background
				in
				<span class="italic">graphic design</span> and photography gives me a unique perspective in crafting
				clean, user-centric digital experiences that are as visually pleasing as they are technically
				sound.
			</p>

			<span
				class="absolute right-4 bottom-0 translate-x-2 translate-y-6 font-serif text-7xl opacity-20 select-none sm:-bottom-14 md:text-9xl lg:bottom-4 lg:translate-y-3"
			>
				”
			</span>
		</div>
	</div>
</div>
