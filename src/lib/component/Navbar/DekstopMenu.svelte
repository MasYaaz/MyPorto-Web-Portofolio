<script>
	import { page } from '$app/state';
	import { navItems } from '$lib/stores/array';
	import { theme } from '$lib/stores/DarkModeStates.svelte';
	import { ui } from '$lib/stores/UIStates.svelte';
</script>

<!-- Desktop Nav -->
{#if page.url.pathname === '/'}
	<nav
		class="hidden h-full items-center justify-center transition-all duration-500 ease-in-out lg:flex"
		class:w-[0%]={ui.firstPageNavbarMode}
		class:w-[75%]={!ui.firstPageNavbarMode}
		class:opacity-0={ui.firstPageNavbarMode}
	>
		{#each navItems as item}
			<button
				onclick={() => ui.scrollToSection(item.id)}
				class=" h-full w-full text-center font-primary text-[13px] font-bold tracking-[1px] whitespace-nowrap uppercase transition-all duration-300 hover:scale-105 hover:cursor-pointer md:text-[15px] lg:mr-10"
				class:scale-110={ui.halamanAktif === item.id}
				class:border-transparent={ui.halamanAktif !== item.id}
				class:text-orange={(ui.halamanAktif === item.id && !theme.darkMode) ||
					(ui.halamanAktif !== item.id && theme.darkMode)}
				class:text-secondary={(ui.halamanAktif !== item.id && !theme.darkMode) ||
					(ui.halamanAktif === item.id && theme.darkMode)}
				class:bg-secondary={ui.halamanAktif === item.id && !theme.darkMode}
				class:bg-orange={ui.halamanAktif === item.id && theme.darkMode}
				aria-label={item.aria}
			>
				{item.label}
			</button>
		{/each}
	</nav>
{/if}
