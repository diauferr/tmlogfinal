<script>
	import Contact from './../lib/Contact.svelte';
	import About from './../lib/About.svelte';
	import Solutions from './../lib/Solutions.svelte';
	import Header from './../lib/Header.svelte';
    import Stats from './../lib/Stats.svelte';
	import data from '../data/data';
</script>

<Header />
<Stats stats={data.STATS} />
<Solutions solutions={data.SOLUTIONS} />
<About about={data.ABOUT}/>
<Contact contact={data.CONTACT}/>

<style>

</style>