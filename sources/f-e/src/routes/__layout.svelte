<script>
  import 'inter-ui/inter.css';
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

    width: var(--editor-width);
  }

  .nav-container {
    grid-area: nav-container;
    display: flex;
    min-height: var(--nav-container-min-height);
  }

  .body-container {
    grid-area: body-container;
    display: flex;
    flex-direction: column;
    overflow: auto;
    align-items: center;
  }

  .footer-container {
    grid-area: footer-container;
    display: flex;
    min-height: var(--footer-container-min-height);
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
