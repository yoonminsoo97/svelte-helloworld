<script>
  import 'bootstrap/dist/css/bootstrap.min.css';
  import Header from '$lib/components/Header.svelte';
  import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
  <title>Hello, Svelte!!</title>
</svelte:head>

<Header />

<div class="container">
  <slot />
</div>

<Footer />