<script lang="ts">
	import DarkmodeButton from './Navbar/DarkmodeButton.svelte';
	import HamburgerButton from './Navbar/HamburgerButton.svelte';
	import DekstopMenu from './Navbar/DekstopMenu.svelte';
	import MobileMenu from './Navbar/MobileMenu.svelte';
	import { ui } from '$lib/stores/UIStates.svelte';
	import HomeButton from './Navbar/HomeButton.svelte';
	import Logo from './Navbar/Logo.svelte';
</script>

<header class="flex w-full justify-center">
	<div
		class:shadow-none={ui.firstPageNavbarMode}
		class:bg-transparent={ui.firstPageNavbarMode}
		class:dark:shadow-none={ui.firstPageNavbarMode}
		class:dark:bg-transparent={ui.firstPageNavbarMode}
		class="fixed top-0 z-50 flex h-18 w-full justify-center bg-primary/90 shadow-xl/50 transition-all duration-200 ease-in lg:h-20 dark:bg-secondary/90"
	>
		<div class="mx-auto flex w-full max-w-7xl justify-between px-6 md:px-16 lg:px-0">
			<Logo />
			<DekstopMenu />

			<div class="flex h-full w-[5%] items-center justify-end gap-4">
				<HomeButton />
				<DarkmodeButton />
				<!-- Hamburger -->
				<HamburgerButton />
			</div>
		</div>
	</div>
	<MobileMenu />
</header>
