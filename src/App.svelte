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

  @layer utilities {
    .h-big {
      height: 700px;
    }

    .flex-right {
      display: flex;
      justify-content: flex-end;
      align-items: center;
    }

    .flex-center {
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .active {
      border-width: 5px;
      border-top: 1px solid lightgreen;
      border-bottom: 1px solid lightgreen;
    }
  }
</style>
