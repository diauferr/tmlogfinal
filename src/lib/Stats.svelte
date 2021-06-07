<script>

export let stats = [];

</script>
<div id="container" class="w-full h-auto flex items-center justify-center">
    <div class="flex flex-col lg:flex-row my-8">
        {#each stats as stat}
        <div class="flex items-center p-4 m-1 text-white">
            <img src={stat.img} alt="">
            <div class="mx-4">
                <h1 class="font-semibold text-3xl">{stat.title}</h1>
                <p class="font-thin">{stat.p}</p>
            </div>
        </div>
        {/each}
    </div>
</div>

<style>

    #container {
        background-color: #0D0D2B;
    }
    
</style>