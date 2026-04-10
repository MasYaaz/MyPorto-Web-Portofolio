<script>
	import image from '$lib/images/profil1.webp';
</script>

<!-- Posisikan ke kanan bawah -->
<div class="absolute right-0 bottom-0 z-0 hidden lg:flex lg:w-[45%] lg:flex-2 lg:justify-start">
	<img
		src={image}
		loading="eager"
		fetchpriority="high"
		alt="Foto Profil Kartun"
		class="pointer-events-none h-auto w-full object-contain transition-all duration-700 select-none hover:scale-105"
	/>
</div>
