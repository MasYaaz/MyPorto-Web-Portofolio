<script lang="ts">
	let { item } = $props();
</script>

<div
	class="flex items-center gap-4 border border-primary/5 bg-white/5 p-4 transition-all hover:border-primary/20"
>
	<img
		src={item.logo}
		alt={item.name}
		class="h-8 w-8 {item.invertDark ? 'dark:invert' : ''} {item.name === 'Ollama'
			? 'rounded-full'
			: ''}"
	/>
	<div class="flex flex-col">
		<span class="text-xs font-bold uppercase">{item.name}</span>
		{#if item.desc}
			<span class="text-[10px] opacity-60">{item.desc}</span>
		{/if}
	</div>
</div>
