<script lang="ts">
	let { item } = $props();
</script>

<div
	class="group relative flex items-center gap-4 border-2 border-primary bg-secondary p-4 shadow-[4px_4px_0px_0px_var(--color-primary)] transition-all
    duration-200 hover:-translate-x-0.5 hover:-translate-y-0.5
    dark:border-secondary dark:bg-primary dark:shadow-[4px_4px_0px_0px_var(--color-secondary)]"
>
	<div
		class="flex h-12 w-12 shrink-0 items-center justify-center border-2 border-primary p-2 transition-transform duration-200
        group-hover:-rotate-3 dark:border-secondary"
		style="
            background-color: {item.color
			? item.color.replace(',0.5)', ',0.15)')
			: 'rgba(0,0,0,0.05)'};
        "
	>
		<img
			src={item.logo}
			alt={item.name}
			class="aspect-square h-full w-full object-contain transition-transform duration-200 group-hover:scale-110
            {item.invertDark ? 'dark:invert' : ''} 
            {item.name === 'Ollama'
				? 'rounded-full border border-primary dark:border-secondary'
				: ''}"
		/>
	</div>

	<div class="flex min-w-0 flex-col gap-0.5 text-primary dark:text-secondary">
		<span
			class="w-fit border-b border-transparent text-xs font-black tracking-wide uppercase transition-colors duration-200
            group-hover:border-primary dark:group-hover:border-secondary"
		>
			{item.name}
		</span>
		{#if item.desc}
			<span class="truncate text-[10px] font-medium opacity-80">
				{item.desc}
			</span>
		{/if}
	</div>

	{#if item.category}
		<span
			class="absolute top-2 right-2 border border-primary bg-aqua px-1 text-[8px] font-black
            tracking-wider text-primary uppercase
            dark:border-secondary dark:bg-orange dark:text-secondary"
		>
			{item.category}
		</span>
	{/if}
</div>
