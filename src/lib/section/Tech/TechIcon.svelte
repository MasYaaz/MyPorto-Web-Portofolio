<script lang="ts">
	let { item } = $props();
</script>

<div
	role="button"
	tabindex="0"
	class="group relative flex flex-col items-center justify-between border-4 border-primary bg-secondary p-5 shadow-[8px_8px_0px_0px_var(--color-primary)] transition-all duration-200 hover:-translate-x-1 hover:-translate-y-1
    focus-visible:-translate-x-1 focus-visible:-translate-y-1 focus-visible:outline-none
    dark:border-secondary dark:bg-primary dark:shadow-[8px_8px_0px_0px_var(--color-secondary)]"
	onmouseenter={(e) => {
		// Cek apakah dokumen sedang berada dalam mode dark
		const isDark = document.documentElement.classList.contains('dark');
		const defaultShadowColor = isDark ? 'var(--color-secondary)' : 'var(--color-primary)';

		// Gunakan item.color saat hover di light mode, atau shadow kontras bawaan di dark mode agar tetap terbaca jelas
		e.currentTarget.style.boxShadow = `12px 12px 0px 0px ${!isDark && item.color ? item.color.replace(',0.5)', ',1)') : defaultShadowColor}`;
	}}
	onmouseleave={(e) => {
		const isDark = document.documentElement.classList.contains('dark');
		e.currentTarget.style.boxShadow = isDark
			? '8px 8px 0px 0px var(--color-secondary)'
			: '8px 8px 0px 0px var(--color-primary)';
	}}
	onfocus={(e) => {
		const isDark = document.documentElement.classList.contains('dark');
		const defaultShadowColor = isDark ? 'var(--color-secondary)' : 'var(--color-primary)';
		e.currentTarget.style.boxShadow = `12px 12px 0px 0px ${!isDark && item.color ? item.color.replace(',0.5)', ',1)') : defaultShadowColor}`;
	}}
	onblur={(e) => {
		const isDark = document.documentElement.classList.contains('dark');
		e.currentTarget.style.boxShadow = isDark
			? '8px 8px 0px 0px var(--color-secondary)'
			: '8px 8px 0px 0px var(--color-primary)';
	}}
>
	<!-- Label Kategori ala Tag Retro (Kiri Atas) -->
	{#if item.category}
		<span
			class="absolute -top-3 -left-3 border-2 border-primary bg-yellow px-2 py-0.5 text-[9px] font-black
            tracking-wider text-primary uppercase
            dark:border-secondary dark:bg-orange dark:text-secondary"
		>
			{item.category}
		</span>
	{/if}

	<!-- Container Logo dengan Border Kotak Kaku -->
	<div
		class="mt-2 flex h-20 w-20 items-center justify-center border-2 border-primary bg-white/80 p-2 transition-transform duration-200
        group-hover:rotate-3 group-focus-visible:rotate-3
        dark:border-secondary dark:bg-zinc-800/90"
	>
		<img
			src={item.logo}
			alt={item.name}
			class="aspect-square h-full w-full object-contain {item.invertDark ? 'dark:invert' : ''}"
		/>
	</div>

	<!-- Informasi Teks Tegas -->
	<div class="mt-4 flex w-full flex-col items-center gap-1">
		<!-- Nama Tech -->
		<span
			class="border-b-2 border-primary pb-0.5 text-center text-xs font-black tracking-wide
            text-primary uppercase
            dark:border-secondary dark:text-secondary"
		>
			{item.name}
		</span>

		<!-- Deskripsi Tech -->
		{#if item.desc}
			<p
				class="mt-1 line-clamp-2 px-1 text-center text-[10px] leading-tight font-medium text-primary
                opacity-80 dark:text-secondary"
			>
				{item.desc}
			</p>
		{/if}
	</div>
</div>
