<script>
  import Typewriter from "svelte-typewriter";
</script>

<section
  id="home"
  style="background-image: url(images/forest.jpeg)"
  class="h-screen bg-nature w-full bg-no-repeat bg-cover bg-center relative font-sans"
>
  <div
    class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2
    w-3/4 md:w-2/5 mx-auto flex justify-center items-center flex-col"
  >
    <!-- <div class="uppercase text-xl">Welcome to my portfolio</div> -->
    <Typewriter interval={50} loop={true}>
      <p class="text-6xl font-serif">Software Engineer</p>
      <p class="text-6xl font-serif">Designer</p>
      <p class="text-6xl font-serif">Entrepreneur</p>
    </Typewriter>
  </div>

  <div
    class="absolute top-3/4 left-1/2 transform -translate-x-1/2 -translate-y-1/2
  w-3/4 md:w-2/5 mx-auto flex justify-center items-center"
  >
    <a
      href="#"
      class="h-6 bg-green-100 w-56 h-20 flex justify-center items-center rounded-2xl hover:bg-green-200 transition duration-200 ease-in-out"
    >
      <button class="text-3xl">Contact Me</button>
    </a>
  </div>
</section>

<style>
</style>
