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
    ? "background-image: url(images/lights.jpeg)"
    : "background-image: url(images/christmas-bg.jpeg)"}
  class="h-screen w-full bg-no-repeat bg-cover bg-right lg:bg-center relative"
>
  {#if y < 500}
    <Snowflakes />
  {/if}
  <div
    class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2
    w-3/4 md:w-2/5 lg:w-2/5 h-40 lg:h-52 mx-auto flex justify-evenly items-center flex-col border-t-2 border-b-2 border-dashed border-white  text-white"
  >
    <h2 class="text-3xl md:4xl lg:text-5xl xl:text-6xl tracking-wide">
      Nico Herrera
    </h2>
    <p class="text-lg md:text-xl lg:text-2xl tracking-wide">
      <Typewriter interval={50} loop={true}>
        <span class="text-lg md:text-xl lg:text-2xl">web</span>
        <span class="text-lg md:text-xl lg:text-2xl ">mobile</span>
        <span class="text-lg md:text-xl lg:text-2xl">full-stack</span>
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
