<script>
  import Typewriter from "svelte-typewriter";
  import Snowflakes from "./Snowflakes.svelte";
  let y;
  let x = window.innerWidth;
</script>

<svelte:window bind:scrollY={y} />

<section
  id="home"
  style={x < 600
    ? "background-image: url(images/outdoor-tree.jpeg)"
    : "background-image: url(images/christmas-bg.jpeg)"}
  class="h-screen w-full bg-no-repeat bg-cover bg-center lg:bg-center relative scroll-snap-y"
>
  {#if y < 500}
    <Snowflakes />
  {/if}
  <div
    class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2
    w-3/4 md:w-2/5 lg:w-2/5 h-40 lg:h-52 mx-auto flex justify-evenly items-center flex-col border-t-2 border-b-2 {x <
    600
      ? 'border-double border-blue-400'
      : 'border-dashed border-white'}  text-white"
  >
    <h2
      class="text-3xl md:4xl lg:text-5xl xl:text-6xl tracking-wide {x < 600
        ? 'bg-blue-400 text-black bg-opacity-90 p-1'
        : 'null'}"
    >
      Nico Herrera
    </h2>
    <p
      class="text-lg md:text-xl lg:text-2xl {x < 600
        ? 'bg-blue-400 text-black bg-opacity-90'
        : 'null'} tracking-wide"
    >
      <Typewriter interval={50} loop={true}>
        <span
          class="text-lg md:text-xl lg:text-2xl {x < 600
            ? 'bg-blue-400 text-black bg-opacity-90'
            : 'null'}">web</span
        >
        <span
          class="text-lg md:text-xl lg:text-2xl {x < 600
            ? 'bg-blue-400 text-black bg-opacity-90'
            : 'null'}">mobile</span
        >
        <span
          class="text-lg md:text-xl lg:text-2xl {x < 600
            ? 'bg-blue-400 text-black bg-opacity-90'
            : 'null'}">full-stack</span
        >
        development
      </Typewriter>
    </p>
  </div>
  <a
    href="#about"
    class="absolute top-60prc left-1/2 transform -translate-x-1/2 -translate-y-1/2 border-2
     border-dotted border-green-400 rounded-md bg-red-500 hover:bg-red-600 w-36 h-12 lg:w-40 lg:h-14
     flex-center
mx-auto"
  >
    <button class="text-white tracking-wide text-base lg:text-xl"
      >About Me</button
    >
  </a>
</section>

<style>
</style>
