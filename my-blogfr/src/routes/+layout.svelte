<script>
	import Header from '$lib/components/Header.svelte';
	import Footer from '$lib/components/Footer.svelte';
	import '../app.css';
</script>


<div class="flex flex-col min-h-screen">
    <Header/>
    <div class="flex-grow mx-10 my-5">
      <slot />
    </div>
    <Footer />
</div>

<style lang="postcss">
  /* main{
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    margin: 0;
  } */
</style>