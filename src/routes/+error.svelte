<script lang="ts">
	import { page } from '$app/state';
	import { Undo2 } from 'lucide-svelte';
	import { fade, fly } from 'svelte/transition';
</script>

<div class="flex min-h-screen w-full items-center justify-center bg-[#F8F5F0] p-4">
	<!-- Card Utama dengan Efek Soft Shadow & Border -->
	<div
		in:fly={{ y: 20, duration: 800 }}
		class="relative flex w-full max-w-md flex-col items-center justify-center overflow-hidden rounded-[40px] border border-white bg-white/50 pt-16 pb-12 shadow-[0_20px_50px_rgba(0,0,0,0.05)] backdrop-blur-md"
	>
		<!-- Background Accent (Lingkaran halus di belakang angka) -->
		<div class="absolute -top-10 -left-10 h-40 w-40 rounded-full bg-primary/5 blur-3xl"></div>

		<!-- Status Code dengan gaya Outline/Minimalist -->
		<h1
			class="relative text-[120px] leading-none font-black tracking-tighter text-primary/10 sm:text-[150px]"
		>
			{page.status}
			<span
				class="absolute inset-0 flex items-center justify-center text-6xl font-bold text-primary sm:text-7xl"
			>
				{page.status}
			</span>
		</h1>

		<div class="mt-8 px-8 text-center">
			<h2 class="font-heading text-2xl font-bold tracking-tight text-primary">
				Oops! Terjadi Kesalahan
			</h2>
			<p class="mt-2 font-medium text-primary/60">
				{page.error?.message ||
					'Halaman yang kamu cari mungkin sedang bersembunyi atau sudah pindah alamat.'}
			</p>
		</div>

		<!-- Tombol Back dengan Hover Effect yang lebih manis -->
		<a
			href="/"
			class="group mt-10 flex items-center justify-center rounded-full bg-primary p-4 text-white transition-all duration-300 hover:scale-110 hover:shadow-lg active:scale-95"
			aria-label="Kembali ke Beranda"
		>
			<Undo2 class="h-6 w-6 transition-transform " />
		</a>

		<!-- Hiasan Kecil di bawah -->
		<div class="mt-8 h-1 w-12 rounded-full bg-primary/20"></div>
	</div>
</div>
