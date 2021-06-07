<script>
	import Navbar from './Navbar.svelte';
</script>

<Navbar />

<div class="w-full flex flex-col lg:flex-row items-center justify-center text-white" id="hero">
	<div class="wraper flex flex-col items-center lg:flex-row">  
	<div class="flex flex-col my-8">
		<h1 class="text-4xl md:text-6xl font-semibold">Logística & tecnologia</h1>
		<h1 class="text-4xl md:text-6xl font-semibold">movimentando seu</h1>
		<h1 class="text-4xl md:text-6xl font-semibold">negócio</h1>
		<br>
		<p class="font-thin">Nós trabalhamos com tecnologia de ponta para simplificar todo processo logístico do seu negócio.</p>
		<br>
		<a class="flex items-center justify-around w-52 h-14 rounded-full px-2" id="btn" href="#">Orçamento AGORA <img src="./arrow-right.svg" alt=""></a>
		<br>
	</div>
	<div>
		<img src="./hero.png" alt="">
	</div>
</div>
</div>

<style>
	#hero {
		background-color: #0D0D2B;
	}

	#btn {
		background-color: #3D4DA1;
	}

	p {
		color: #E0E0E0;
		opacity: 0.8;
	}

	img {
		mix-blend-mode: color-dodge;
	}

	.wraper {
		max-width: 80%;	
	}
</style>
