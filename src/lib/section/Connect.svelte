<script lang="ts">
	import Back1 from '$lib/component/Background/Back1.svelte';
	import github from '$lib/logo/github.svg';
	import shutterstock from '$lib/logo/shutterstock.svg';

	const socialLinks = [
		{
			name: 'Github',
			label: 'Github',
			href: 'https://github.com/MasYaaz',
			icon: github,
			shouldInvert: true
		},
		{
			name: 'Assets',
			label: 'Assets',
			href: 'https://www.shutterstock.com/g/MasYaaz',
			icon: shutterstock,
			shouldInvert: false
		}
	];
</script>

<section
	class="relative flex min-h-screen w-full flex-col items-center justify-center gap-12 py-20 lg:py-0"
	id="section_5"
>
	<Back1 />
	<div class="z-10 px-6 text-center">
		<h2 class="mb-4 font-primary text-3xl font-black text-primary lg:text-5xl dark:text-secondary">
			Mari Berkolaborasi
		</h2>
		<p class="font-display text-primary dark:text-secondary">
			Mau lihat porto yang ku miliki, cari disini ya..!
		</p>
	</div>

	<div class="z-10 container grid max-w-7xl grid-cols-1 gap-8 px-6 md:grid-cols-2 md:px-16 lg:px-0">
		{#each socialLinks as link}
			<a
				href={link.href}
				target="_blank"
				class="group flex flex-col items-center p-8 transition-all"
			>
				<img
					src={link.icon}
					alt={link.name}
					class="mb-4 h-20 w-20 transition-transform group-hover:scale-110 lg:h-16 lg:w-16"
					class:dark:invert={link.shouldInvert}
					loading="lazy"
				/>
				<span class="font-bold text-primary dark:text-secondary">{link.label}</span>
			</a>
		{/each}
	</div>

	<p class="mt-20 font-primary text-primary italic opacity-50 dark:text-secondary">
		-- Thanks for your attention --
	</p>
</section>
