<script lang="ts">
	import Back2 from '$lib/component/Background/Back2.svelte';
	import SectionTitle from '$lib/component/UIComponent/SectionTitle.svelte';
	import TechCard from './Tech/TechCard.svelte';
	import TechIcon from './Tech/TechIcon.svelte';
	import yolo from '$lib/logo/yolo.svg';
	import ci4 from '$lib/logo/ci4.svg';

	// Array data untuk Core Technologies yang sudah diperbarui
	const techStack = [
		// === DEVELOPMENT ===
		{
			name: 'SvelteKit',
			logo: 'https://raw.githubusercontent.com/sveltejs/branding/master/svelte-logo.svg',
			category: 'dev',
			color: 'rgba(255,62,0,0.5)',
			desc: 'Svelte 5 & Runes Full-stack Development'
		},
		{
			name: 'TypeScript',
			logo: 'https://www.vectorlogo.zone/logos/typescriptlang/typescriptlang-icon.svg',
			category: 'dev',
			color: 'rgba(49,120,198,0.5)',
			desc: 'Type-safe JavaScript Development'
		},
		{
			name: 'Bun',
			logo: 'https://www.vectorlogo.zone/logos/bunsh/bunsh-icon.svg',
			category: 'dev',
			color: 'rgba(251,203,142,0.5)',
			desc: 'Fast JavaScript Runtime & Package Manager'
		},
		{
			name: 'CodeIgniter 4',
			logo: ci4,
			category: 'dev',
			color: 'rgba(238,67,39,0.5)',
			desc: 'Lightweight & Fast PHP Framework for MVC Applications'
		},
		{
			name: 'PHP',
			logo: 'https://www.vectorlogo.zone/logos/php/php-icon.svg',
			category: 'dev',
			color: 'rgba(119,123,179,0.5)',
			desc: 'Server-side Scripting Language & Modern Backend Development'
		},
		{
			name: 'Tauri',
			logo: 'https://icon.icepanel.io/Technology/svg/Tauri.svg',
			category: 'dev',
			color: 'rgba(36,195,243,0.5)',
			desc: 'Build Tiny, Fast Desktop Apps with Web Tech & Rust'
		},
		{
			name: 'Rust',
			logo: 'https://www.rust-lang.org/static/images/rust-logo-blk.svg',
			category: 'dev',
			color: 'rgba(0,0,0,0.5)',
			invertDark: true,
			desc: 'High-performance Backend & Systems'
		},
		{
			name: 'Python',
			logo: 'https://www.vectorlogo.zone/logos/python/python-icon.svg',
			category: 'dev',
			color: 'rgba(55,118,171,0.5)',
			desc: 'Data Science, Machine Learning & Scripting Ecosystem'
		},
		{
			name: 'Tailwind CSS',
			logo: 'https://www.vectorlogo.zone/logos/tailwindcss/tailwindcss-icon.svg',
			category: 'dev',
			color: 'rgba(6,182,212,0.5)',
			desc: 'Modern Utility-First CSS (v4 Stack)'
		},

		// === DATABASES & BACKEND ===
		{
			name: 'Supabase',
			logo: 'https://raw.githubusercontent.com/supabase/supabase/master/packages/common/assets/images/supabase-logo-icon.svg',
			category: 'database',
			color: 'rgba(62,175,124,0.5)',
			desc: 'PostgreSQL, Authentication & Realtime Sync'
		},
		{
			name: 'MariaDB',
			logo: 'https://mariadb.com/wp-content/uploads/2019/11/mariadb-logo-vertical_black.svg',
			category: 'database',
			color: 'rgba(0,53,99,0.5)',
			invertDark: true,
			desc: 'Robust Relational Database Management System'
		},

		// === AI & COMPUTER VISION ===
		{
			name: 'Ollama',
			logo: 'https://unpkg.com/@lobehub/icons-static-svg@latest/icons/ollama.svg',
			category: 'ai',
			invertDark: true,
			desc: 'Local LLM Deployment (DeepSeek, Qwen, Llama)'
		},
		{
			name: 'YOLO',
			logo: yolo,
			category: 'ai',
			color: 'rgba(13,110,253,0.5)',
			desc: 'Computer Vision & Real-time Object Detection'
		},

		// === TOOLS ===
		{
			name: 'Git',
			logo: 'https://www.vectorlogo.zone/logos/git-scm/git-scm-icon.svg',
			category: 'tool',
			desc: 'Distributed Version Control'
		},
		{
			name: 'VS Code',
			logo: 'https://www.vectorlogo.zone/logos/visualstudio_code/visualstudio_code-icon.svg',
			category: 'tool',
			desc: 'Primary Code Editor'
		}
	];

	// Reactive states menggunakan Svelte 5 Runes
	const Devs = $derived(techStack.filter((i) => i.category === 'dev'));
	const databases = $derived(techStack.filter((i) => i.category === 'database'));
	const aiTechs = $derived(techStack.filter((i) => i.category === 'ai'));
	const tools = $derived(techStack.filter((i) => i.category === 'tool'));
</script>

<section
	class="relative flex min-h-screen w-full flex-col items-center justify-center gap-8 bg-secondary py-16 md:pt-30 dark:bg-primary"
	id="section_3"
>
	<Back2 />
	<div
		class="z-10 container mx-auto flex w-full max-w-7xl flex-col items-center gap-8 px-6 text-primary dark:text-secondary"
	>
		<SectionTitle title="Tech Stack" />
		<div
			class="scallop-box w-full space-y-10 border-4 border-primary bg-secondary p-8 shadow-[8px_8px_0_0_#000] dark:border-secondary dark:bg-primary dark:shadow-[8px_8px_0_0_#F5E6BE]"
		>
			<!-- Web Development Section -->
			<div class="space-y-4">
				<h3
					class="text-center font-display text-xs font-black tracking-[0.2em] text-orange uppercase md:text-left dark:text-secondary"
				>
					Development & Runtime
				</h3>
				<div class="grid grid-cols-1 gap-4 sm:grid-cols-3">
					{#each Devs as item}
						<TechIcon {item} />
					{/each}
				</div>
			</div>

			<!-- Sub-Kategori Lainnya (Ganti ke md:grid-cols-3 agar pas 3 kolom) -->
			<div class="grid grid-cols-1 gap-8 md:grid-cols-3">
				<!-- AI Section -->
				<div class="space-y-4">
					<h3
						class="text-center font-display text-xs font-black tracking-[0.2em] text-orange uppercase md:text-left dark:text-secondary"
					>
						Models
					</h3>
					<div class="flex flex-col gap-3">
						{#each aiTechs as item}
							<TechCard {item} />
						{/each}
					</div>
				</div>

				<!-- Database Section (Tambahan Baru) -->
				<div class="space-y-4">
					<h3
						class="text-center font-display text-xs font-black tracking-[0.2em] text-orange uppercase md:text-left dark:text-secondary"
					>
						Databases
					</h3>
					<div class="flex flex-col gap-3">
						{#each databases as item}
							<TechCard {item} />
						{/each}
					</div>
				</div>

				<!-- Tools Section -->
				<div class="space-y-4">
					<h3
						class="text-center font-display text-xs font-black tracking-[0.2em] text-orange uppercase md:text-left dark:text-secondary"
					>
						Tools & Workflow
					</h3>
					<div class="flex flex-col gap-3">
						{#each tools as item}
							<TechCard {item} />
						{/each}
					</div>
				</div>
			</div>
		</div>
	</div>
</section>
