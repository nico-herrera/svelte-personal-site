<script>
  import Hero from "./components/Hero.svelte";
  import Nav from "./components/Nav.svelte";
  import About from "./components/About.svelte";
  import Services from "./components/Services.svelte";
  import Contact from "./components/Contact.svelte";
  import Footer from "./components/Footer.svelte";
</script>

<div>
  <Nav />
  <Hero />
  <About />
  <Services />
  <Contact />
  <Footer />
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

    .smooth-scroll {
      scroll-behavior: smooth;
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
    .snowframe {
      position: absolute;
      top: 0;
      right: 0;
      bottom: 0;
      left: 0;
      overflow: hidden;
    }
    .snowflake {
      color: #fff;
      font-size: 1.2rem;
      line-height: 1.2rem;
      font-family: Arial, sans-serif;
      text-shadow: 0 0 5px #000;
      position: absolute;
      z-index: 1000;
      overflow: hidden;
    }

    .top-60prc {
      top: 65%;
    }

    .negtop-30perc {
      top: -27%;
    }

    .negtop-8perc {
      top: -13%;
    }

    .ht-600 {
      height: 600px;
    }

    .scroll-snap-y {
      scroll-snap-type: y;
    }

    .h-10perc {
      height: 10%;
    }

    .h-90perc {
      height: 90%;
    }
  }

  @layer base {
    @font-face {
      font-family: sans-serif;
      font-weight: 400;
      src: url("https://fonts.googleapis.com/css2?family=Inter&display=swap")
        format("inter");
    }
  }
</style>
