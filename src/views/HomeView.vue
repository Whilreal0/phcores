<script setup>
import Services from './Services.vue';

</script>

<template>
  <main
    class="relative bg-gradient-navy-blue h-[75vh] flex flex-col items-center justify-center px-2 md:text-center text-white"
  >
    <div class="flex flex-col items-center gap-2.5 md:max-w-[65vw] ">
      <h1 class="text-5xl font-bold mb-4">Empowering Brands with Digital Innovation</h1>
      <div class="md:max-w-[600px] mx-auto">
          <span class="">
          We provide cutting-edge technology solutions to help your business grow
          and succeed in the digital age. Our team of experts is dedicated to
          delivering high-quality services that meet your specific needs.
        </span>
      </div>
    <div class="flex w-full md:justify-center gap-3">
      <button class="px-8 py-3 semibold rounded-md bg-[#00c2ff] cursor-pointer">Get Started</button>
      <button class="px-8 py-3 semibold rounded-md bg-transparent outline-2 cursor-pointer">Learn More</button>
    </div>
    </div>
  </main>
  <Services/>
</template>
