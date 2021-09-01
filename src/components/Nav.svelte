<script>
  let y;
</script>

<!-- Create Navbar Menu -->
<header
  class="{y > 50
    ? 'bg-white shadow-xl'
    : null} w-full p-5 fixed top-0 z-50 transition duration-500 ease-in-out font-sans"
>
  <nav class="flex items-center justify-between p-6 h-16">
    <div
      class="sm:text-lg lg:text-3xl {y > 50
        ? 'text-green-500'
        : 'text-black'} font-semibold "
    >
      Nico Herrera
    </div>
    <ul>
      <li class="space-x-5 text-2xl font-semibold">
        <a
          href="#home"
          class="hidden sm:inline-block transition duration-200 ease-in-out {y >
          50
            ? 'text-black hover:text-green-500'
            : 'text-black hover:text-green-700'} hover:cursor-pointer">Home</a
        >
        <a
          href="#about"
          class="hidden sm:inline-block transition duration-200 ease-in-out {y >
          50
            ? 'text-black hover:text-green-500'
            : 'text-black hover:text-green-700'} hover:cursor-pointer">About</a
        >
        <a
          href="#"
          class="hidden sm:inline-block transition duration-200 ease-in-out {y >
          50
            ? 'text-black hover:text-green-500'
            : 'text-black hover:text-green-700'} hover:cursor-pointer"
          >Services</a
        >
        <a
          href="#"
          class="hidden sm:inline-block transition duration-200 ease-in-out {y >
          50
            ? 'text-black hover:text-green-500'
            : 'text-black hover:text-green-700'} hover:cursor-pointer"
          >Contact</a
        >
      </li>
      <div class="sm:hidden space-y-1 hover:cursor-pointer">
        <span class="w-10 h-1 bg-gray-600 rounded-full block" />
        <span class="w-10 h-1 bg-gray-600 rounded-full block" />
        <span class="w-10 h-1 bg-gray-600 rounded-full block" />
      </div>
    </ul>
  </nav>
</header>

<svelte:window bind:scrollY={y} />
