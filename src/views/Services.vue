<script setup>
 import {ref} from 'vue'

 const cards = ref([
  {
    name: 'Cloud Solutions',
    description: 'Scalable and secure cloud services to optimize your business operations and enhance productivity.',
    icon: '☁️'
  },
  {
    name: 'Software Development',
    description: 'Custom software solutions tailored to your specific business requirements and industry standards.',
    icon: '💻'
  },
  {
    name: 'Network Security',
    description: 'Comprehensive security measures to protect your valuable data and ensure business continuity.',
    icon: '🔒'
  },
 ])
</script>
<template>
  <div class="h-screen text-center mt-10">
    <h1 class="text-5xl">Our Services</h1>

<!-- Cards -->
<div class="flex justify-center gap-6 flex-wrap px-2">
      <div
        v-for="(card, i) in cards"
        :key="i"
        class="bg-white shadow-lg rounded-md p-6 w-80 hover:shadow-xl transition"
      >
        <div class="text-4xl mb-4">{{ card.icon }}</div>
        <h2 class="text-xl font-semibold mb-2">{{ card.name }}</h2>
        <p class="text-gray-600">{{ card.description }}</p>
      </div>
    </div>
    <!-- Cards -->  
  </div>
</template>
