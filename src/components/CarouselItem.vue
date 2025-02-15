<script setup lang="ts">
import { defineProps } from 'vue'

const props = defineProps({
  icon: {
    type: Object,
    required: true,  
  },
  title: {
    type: String,
    required: true,  
  },
  date: {
    type: String,
    required: true,  
  },
  description: {
    type: String,
    required: true,  
  },
})
</script>

<template>
    <swiper-slide class="w-full flex flex-col items-center justify-center">
        <component :is="props.icon" class="w-16 h-16 mx-auto mb-6 text-[#f58428]"/>

        <h3 class="text-2xl font-bold text-[#14467c] mb-2">{{ props.title }}</h3>

        <p class="text-gray-500 mb-4">{{ props.date }}</p>

        <p class="text-gray-700 text-lg text-center max-w-lg mb-6">
            {{ props.description }}
        </p>

      <button class="p-0 bg-[#f58428] px-4 py-2 rounded cursor-pointer text-white disabled:cursor-not-allowed disabled:opacity-60 font-semibold" disabled>Saiba mais</button>

    </swiper-slide>
</template>