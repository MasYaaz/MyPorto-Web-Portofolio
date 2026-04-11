<script>
	import SectionTitle from '$lib/component/UIComponent/SectionTitle.svelte';
	import chatbot from '$lib/images/chatbot.webp';
	import regis from '$lib/images/regis.webp';
	import porto from '$lib/images/porto.webp';

	// Contoh data project - Nantinya ini bisa kamu pindahkan ke file konstanta
	const projects = [
		{
			title: 'WhatsApp Chatbot AI',
			pict: chatbot,
			description:
				'Chatbot pintar menggunakan Ollama untuk integrasi AI lokal dengan fitur message buffering.',
			tech: ['Bun', 'Ollama', 'Qwen 2.5', 'WhatsApp Web JS'],
			status: 'local',
			github: '#',
			live: ''
		},
		{
			title: 'Tabligh Akbar IKPM Registration System',
			pict: regis,
			description:
				'Sistem manajemen event terpadu dengan fitur check-in QR Code dan dashboard admin multi-role untuk efisiensi registrasi peserta secara realtime.',
			tech: ['SvelteKit', 'TailwindCSS', 'Supabase', 'Qr Scanner'],
			status: 'online',
			github: '#',
			live: 'https://tablighakbar2026.netlify.app/login'
		},
		{
			title: 'My Porto Web',
			pict: porto,
			description:
				'Website portofolio yang kamu buka sekarang ini yang menerapkan konsep svelte runes secara konsisten.',
			tech: ['Sveltekit'],
			status: 'online',
			github: '#',
			live: 'https://myportowebportofolio.netlify.app'
		}
	];
</script>

<section
	id="section_4"
	class="relative flex min-h-screen w-full items-center bg-secondary py-20 dark:bg-primary"
>
	<div
		class="z-10 mx-auto flex max-w-7xl flex-col items-center px-6 transition-all duration-700 ease-out lg:px-0"
	>
		<div class="mb-12 text-center">
			<SectionTitle title="Featured Projects" />
			<p class="mt-4 max-w-2xl font-display text-primary dark:text-secondary">
				Berikut adalah beberapa proyek pengembangan web dan sistem yang telah saya kerjakan
				baru-baru ini.
			</p>
		</div>

		<div class="grid grid-cols-1 gap-8 md:grid-cols-2 lg:grid-cols-3">
			{#each projects as project}
				<div
					class="group scallop-box relative flex flex-col border-4 border-orange bg-white p-6 transition-all hover:-translate-y-2 dark:border-secondary dark:bg-slate-900"
				>
					<img
						alt="Project foto pict"
						src={project.pict}
						class="mb-2 aspect-3/2 w-full object-cover"
					/>
					<h3 class="mb-2 font-primary text-xl font-bold text-primary dark:text-secondary">
						{project.title}
					</h3>

					<p class="mb-6 grow text-justify font-display text-sm text-primary dark:text-secondary">
						{project.description}
					</p>

					<div class="mb-6 flex flex-wrap gap-2">
						{#each project.tech as item}
							<span
								class="rounded-md bg-secondary px-2 py-1 text-xs font-medium text-slate-700 dark:bg-slate-800 dark:text-slate-300"
							>
								{item}
							</span>
						{/each}
					</div>

					<div class="flex items-center gap-4">
						<div class="flex items-center gap-2">
							{#if project.status === 'online'}
								<span class="flex h-2 w-2 rounded-full bg-green-500"></span>
								<span class="text-[10px] font-bold text-green-500 uppercase">Live</span>
							{:else if project.status === 'local'}
								<span class="flex h-2 w-2 rounded-full bg-orange-500"></span>
								<span class="text-[10px] font-bold text-orange-500 uppercase">local</span>
							{/if}
						</div>
						<div class="flex items-center gap-2">
							{#if project.github}
								<a
									href={project.github}
									target="_blank"
									rel="noopener noreferrer"
									class="transition-transform hover:scale-110"
									title="View Source Code"
								>
									<img
										src="https://cdn.jsdelivr.net/npm/simple-icons@v13/icons/github.svg"
										alt="GitHub"
										class="h-6 w-6 object-contain dark:invert"
									/>
								</a>
							{/if}
							{#if project.live}
								<a
									href={project.live}
									target="_blank"
									class="hover:bg-opacity-80 rounded-lg bg-primary px-4 py-2 text-xs font-bold text-white transition-colors dark:bg-secondary dark:text-primary"
								>
									Live Demo
								</a>
							{/if}
						</div>
					</div>
				</div>
			{/each}
		</div>
	</div>
</section>
