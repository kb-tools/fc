<script>
  import '../global.css';
  import Nav from '$lib/components/Nav/index.svelte';
  import Footer from '$lib/components/Footer/index.svelte';
</script>

<style>
  .main-container {
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: auto 1fr auto;
    grid-template-areas:
      'nav-container'
      'body-container'
      'footer-container'
    ;
    gap: var(--main-gap);
    height: 100vh;
  }

  .nav-container {
    grid-area: nav-container;
    display: flex;
  }

  .body-container {
    grid-area: body-container;
    display: flex;
    flex-direction: column;
    overflow: auto;

    background-color: red;
  }

  .footer-container {
    grid-area: footer-container;
    display: flex;
  }
</style>

<div class='main-container'>
  <section class='nav-container'>
    <Nav />
  </section>
  <main class='body-container'>
    <slot></slot>
  </main>
  <section class='footer-container'>
    <Footer />
  </section>
</div>
