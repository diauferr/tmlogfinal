<script>
	import { each } from 'svelte/internal';

export let about = [];

</script>

<div id="container" class="w-full h-auto text-white text-center flex flex-col items-center">
    <h1 class="text-4xl font-semibold py-2">Quem somos nós?</h1>
    <p class="font-thin my-8 max-w-md">Somos uma empresa com foco em ajudar os clientes a tomar as melhores decisões no ramo de agenciamento de cargas.</p>
    <div class="flex flex-col items-center bg-white rounded-xl font-darkblue text-center max-w-md lg:max-w-xl px-8 shadow-lg">
        <p class="py-8 md:max-w-xl">Com o início das operações no brasil em 2021 amparado por um time com expertise em agenciamento temos como objetivo oferecer aos nossos clientes análises de cada projeto integrando viabilidade e segurança.</p>
        <p class="py-8 md:max-w-xl">Nosso departamento de coordenação possui amplo conhecimento, gerenciando os embarques de ponta a ponta, fazendo com que os projetos fluam de forma ágil e eficaz de acordo com o perfil de cada cliente, prestando todo auxílio e suporte necessário do início ao fim do processo.</p>
    </div>
    <h1 class="text-4xl font-semibold py-8">Conheça nossos valores:</h1>
    <div class="flex flex-col justify-around lg:flex-row">
        {#each about as item }
        <div class="card m-8 p-4 max-w-sm rounded-xl">
            <h1 class="py-3 text-2xl font-semibold">{item.title}</h1>
            <p class="font-thin">{item.p}</p>
        </div>
        {/each}
    </div>
</div>

<style>
    #container {
        background: rgb(13,13,43);
        background: linear-gradient(180deg, rgba(13,13,43,1) 0%, rgba(61,77,161,1) 100%);
    }

    .font-darkblue {
        color: #0D0D2B;
    }

    .card {
        background-color: #3D4DA1;
        opacity: 0.9;
    }
</style>