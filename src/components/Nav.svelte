<script>
  import BurgerMenu from "svelte-burger-menu";
  let y;
  let x = window.innerWidth;
</script>

<svelte:window bind:scrollY={y} />

<!-- Create Navbar Menu -->
<header
  class="{y > 50
    ? 'bg-white shadow-lg'
    : 'bg-black bg-opacity-30'} w-full p-1 lg:p-5 fixed top-0 z-50 transition duration-500 ease-in-out"
>
  <nav
    class="flex items-center justify-around p-6 h-16 lg:h-16 flex-row space-x-4"
  >
    <div
      class="{y > 50 ? 'text-green-500' : 'text-white'} {x < 600
        ? 'hidden'
        : null} text-xl md:text-2xl lg:text-3xl "
    >
      Nico Herrera
    </div>
    <ul>
      {#if x < 600}
        <div class="absolute top-3 left-0 ">
          <BurgerMenu
            width="225px"
            backgroundColor="#EF4444"
            burgerColor="#10B981"
            menuColor="#10B981"
            paddingTop="50px"
          >
            <div class="flex justify-evenly items-center flex-col ">
              <a href="#home" class="text-white text-3xl p-2">Home</a>
              <a href="#about" class="text-white text-3xl p-2 ">About</a>
              <a href="#services" class="text-white text-3xl p-2">Services</a>
              <a href="#contact" class="text-white text-3xl p-2">Contact</a>
            </div>
          </BurgerMenu>
        </div>
      {/if}
      <li class="space-x-4 text-xl lg:text-2xl {x < 600 ? 'hidden' : null}">
        <a
          href="#home"
          class="transition duration-100 ease-in-out {y > 50
            ? 'text-black hover:text-green-500'
            : 'text-white hover:text-green-600'} hover:cursor-pointer">Home</a
        >
        <a
          href="#about"
          class="transition duration-100 ease-in-out {y > 50
            ? 'text-black hover:text-green-500'
            : 'text-white hover:text-green-600'} hover:cursor-pointer">About</a
        >
        <a
          href="#services"
          class="transition duration-100 ease-in-out {y > 50
            ? 'text-black hover:text-green-500'
            : 'text-white hover:text-green-600'} hover:cursor-pointer"
          >Services</a
        >
        <a
          href="#contact"
          class="transition duration-100 ease-in-out {y > 50
            ? 'text-black hover:text-green-500'
            : 'text-white hover:text-green-600'} hover:cursor-pointer"
          >Contact</a
        >
      </li>
    </ul>
  </nav>
</header>
