<script>
	import bgLight from '$lib/images/bg-2-light.webp';
	import bgDark from '$lib/images/bg-2-dark.webp';
</script>

<div
	class="hero-bg absolute inset-0 h-full w-full"
	style="--bg-light: url({bgLight}); --bg-dark: url({bgDark});"
></div>

<style>
	.hero-bg {
		background-image: var(--bg-light);
		background-size: cover;
		background-position: center;
		background-repeat: no-repeat;
		transition: background-image 0.3s ease-in-out; /* Opsional: transisi halus saat ganti tema */
	}

	/* Saat parent (html/body) memiliki class .dark */
	:global(.dark) .hero-bg {
		background-image: var(--bg-dark);
	}
</style>
