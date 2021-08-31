<script>
  import Hero from "./components/Hero.svelte";
  import Nav from "./components/Nav.svelte";
</script>

<main class="relative">
  <Nav />
  <Hero />
</main>

<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
</style>
