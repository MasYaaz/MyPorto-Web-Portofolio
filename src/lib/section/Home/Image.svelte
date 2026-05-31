<script>
	import image from '$lib/images/profil-1.webp';
</script>

<!-- Posisikan ke kanan bawah -->
<div class="z-0 flex px-10 lg:w-[80%]">
	<img
		src={image}
		loading="eager"
		fetchpriority="high"
		alt="Foto Profil Kartun"
		class="pointer-events-none h-auto w-full object-contain transition-all duration-700 select-none hover:scale-105"
	/>
</div>
