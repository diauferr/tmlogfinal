<script>
	import Footer from './../../lib/Footer.svelte';
    let clicked = false;
    function menu() {
        if(clicked == false) {
            menuOpen();
        } else {
            menuClose();
        }
    }

    function menuOpen() {
        console.log('OPEN');
        clicked = true;
        let menu = document.querySelector('#menuMobile');
        menu.style.display = 'flex';
    }

    function menuClose() {
        console.log('CLOSE');
        clicked = false;
        let menu = document.querySelector('#menuMobile');
        menu.style.display = 'none';
    }

    import translations from '../../data/translations';
    import { dict, locale, t } from '../../data/i18n';
    $: languages = Object.keys(translations);
    $: dict.set(translations);

</script>
<nav class="w-full h-40 flex justify-around items-center">
    <img src="../logo-full-white.svg" alt="" class="">
    <ul class="hidden sm:flex justify-around items-center">
        {#each $t('navbar') as item}
        <li class="m-8 font-thin">
            <a href="{item.path}">{item.label}</a>
        </li>
        {/each}
        <li class="mr-2 md:mr-4 lg:mr-11" id="divisor">|</li>
        <a href="#" class=""><li class="mr-2 md:mr-4 lg:mr-11 px-8 py-3 rounded-full" id="contact-btn">{$t('contact')}</li></a>
        <select bind:value={$locale} class="uppercase text-white" id="btn-lang">
            {#each languages as lang}
              <option value={lang} class="uppercase flex items-center justify-center">
                {lang}
              </option>
            {/each}
        </select>
    </ul>
    <button class="sm:hidden" on:click={menu}>
        {#if clicked == false}
        <img src="./menu.svg" alt="">
        {:else}
        <img src="./menu-close.svg" alt="">
        {/if}
    </button>
</nav>
<ul class="hidden flex flex-col items-center bg-black" id="menuMobile">
    {#each $t('navbar') as item}
    <li class="my-8 font-thin">
        <a href="{item.path}">{item.label}</a>
    </li>
    {/each}
</ul>
<h1 id="navigation" class="text-white px-8 py-4 font-thin">Início > Soluções > Logística Integrada</h1>
<div id="custom" class="w-full flex flex-col items-center justify-center">
    <img src="../custom-desc.png" alt="">
        <div class="flex flex-col lg:flex-row">
            <div>
                <h1 class="text-white text-2xl font-semibold max-w-lg text-center my-12 px-4">Nossa solução em logística integrada possui o acompanhamento a manuseio da sua carga do inicio ao fim.</h1>
                <ul class="text-white">
                    <li class="flex flex-row items-center my-8"><img id="icon" class="mx-4" src="../check.svg" alt="">Coleta da Carga na fábrica </li>
                    <li class="flex flex-row items-center my-8"><img id="icon" class="mx-4" src="../check.svg" alt="">Recebimento da carga em nosso WH</li>
                    <li class="flex flex-row items-center my-8"><img id="icon" class="mx-4" src="../check.svg" alt="">Conferência e separação dos volumes</li>
                    <li class="flex flex-row items-center my-8"><img id="icon" class="mx-4" src="../check.svg" alt="">Desembaraço aduaneiro (origem e destino)</li>
                    <li class="flex flex-row items-center my-8"><img id="icon" class="mx-4" src="../check.svg" alt="">Entrega da carga no destino final </li>
                </ul>
            </div>
            <div class="flex flex-col items-center justify-center">
                <h2 class="text-white text-xl font-thin my-8 max-w-md text-center">Sua carga sendo coletada e entregue com segurança, agilidade e acompanhamento de ponta a ponta.</h2>
                <h2 class="text-white py-4">Quer saber mais? <a class="btn" href="#">Consulte-nos.</a></h2>
            </div>
        </div>
</div>
<Footer />
<style>

    img {
        mix-blend-mode: lighten;
    }

    #icon {
        width: 30px;
    }

    #custom {
        background-color: #0D0D2B;
    }

    #navigation {
        background-color: #0D0D2B;
    }

    .btn {
        color: #44B6C9;
    }

    #btn-lang {
        background-color: #0D0D2B;
    }
    li {
        color: #fff;
    }
    nav {
        background-color: #0D0D2B;
    }

    #contact-btn {
        background-color: #3D4DA1;
    }

    #contact-btn:hover {
        background-color: #324084;
    }
    
    #divisor {
        color: #F2F2F2 !important;
        opacity: 0.3;
    }

    button {
        width: 50px;
    }

    #menuMobile {
        background-color: #0D0D2B;
        animation-name: open;
        animation-duration: 2s;
        animation-iteration-count: 1;
        animation-fill-mode: forwards;
    }

    @keyframes open {
        0%   {background-color:#0D0D2B; height: 0px;}
        100% {background-color:#0D0D2B; height: 250px;}
    }

</style>