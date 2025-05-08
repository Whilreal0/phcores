<script setup>
import { onMounted, ref , onUnmounted } from "vue";

const isSticky = ref(false);
const trigger = ref(null);

let observer = null;

onMounted(() => {
  observer = new IntersectionObserver(([entry]) => {
    isSticky.value = !entry.isIntersecting;
  });

  if (trigger.value) {
    observer.observe(trigger.value);
  }
});

onUnmounted(() => {
  if (observer && trigger.value) {
    observer.unobserve(trigger.value);
  }
});
</script>

<template>
  <nav :class="['w-full transition-colors duration-500 z-50', isSticky ? 'fixed top-0 bg-[#0A2240] shadow-lg' : 'absolute bg-transparent ']">
    <div class="flex justify-between max-w-[1150px] w-full mx-auto py-7.5 px-2">
      <div class=" flex items-center h-3 md:h-12 text-white ">
       <!-- <img src="/src/assets/logo.png" alt=""> -->
       <span>PH CORE SOLUTIONS</span>
      </div>
      <div class="md:flex items-center hidden">
        <ul class="flex gap-7 font-semibold text-base">
          <li class="cursor-pointer"><a href=""></a>Home</li>
          <li class="cursor-pointer"><a href=""></a>Services</li>
          <li class="cursor-pointer"><a href=""></a>Pricing</li>
          <li class="cursor-pointer"><a href=""></a>About</li>
        </ul>
      </div>
    </div>
  </nav>
  <!-- Empty dummy div to watch -->
  <div ref="trigger" class="h-0"></div>
</template>
