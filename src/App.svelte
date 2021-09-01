<script>
  import Hero from "./components/Hero.svelte";
  import Nav from "./components/Nav.svelte";
  import About from "./components/About.svelte";
</script>

<div>
  <Nav />
  <Hero />
  <About />
</div>

<style global>
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  html {
    scroll-behavior: smooth;
  }
</style>
