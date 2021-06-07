<script>

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

</script>

<nav class="w-full h-40 flex justify-around items-center">
    <img src="./logo-full-white.svg" alt="" class="">
    <ul class="hidden sm:flex justify-around items-center">
        <li class="mr-2 md:mr-4 lg:mr-11"><a href="#">Início</a></li>
        <li class="mr-2 md:mr-4 lg:mr-11"><a href="#">Soluções</a></li>
        <li class="mr-2 md:mr-4 lg:mr-11"><a href="#">Sobre</a></li>
        <li class="mr-2 md:mr-4 lg:mr-11" id="divisor">|</li>
        <a href="#" class=""><li class="btn mr-2 md:mr-4 lg:mr-11 px-8 py-3 rounded-full" id="contact-btn">Contato</li></a>
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
    <li class="my-8"><a href="#">Início</a></li>
    <li class="my-8"><a href="#">Soluções</a></li>
    <li class="my-8"><a href="#">Sobre</a></li>
    <li class="my-8"><a href="#" class="">Contato</a></li>
</ul>

<style>
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
        100% {background-color:#0D0D2B; height: 350px;}
    }
</style>