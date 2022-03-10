<script>
  import Header from "$lib/components/Header.svelte";
  import Footer from "$lib/components/Footer.svelte";
  import "../app.css";
</script>

<main>
  <div>
    <Header />
    <slot />
  </div>
  <Footer />
</main>

<style>
  main {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }

  div {
    flex: 1;
  }
</style>
