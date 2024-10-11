<script>
  import { page } from '$app/stores';

  const links = [
    {href: '/', text: 'Home'},
    {href: '/about', text: 'About'},
    {href: '/login', text: 'Login'},
    {href: '/signup', text: 'Signup'},
  ];
</script>

<header class="shadow-sm">
  <div class="container">
    <nav class="d-flex justify-content-center py-3">
      {#each links as {href, text}}
        <a href={href} class:active={$page.url.pathname === href}>
          {text}
        </a>
      {/each}
    </nav>
  </div>
</header>

<style>
  nav {
    display: flex;
    gap: 2rem;
  }

  nav a {
    text-decoration: none;
    color: black;
  }

  nav a.active {
    color: #0d6efd;
  }
</style>