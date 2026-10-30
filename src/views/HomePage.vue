<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Jacob Reyna',
  slogan: 'Game Designer in the Making',
  avatar: new URL('@/assets/Profile.jpeg', import.meta.url).href
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!--Profile Header-->
    <div class="mb-8 flex flex-col items-center">
      <div 
      class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-lime-400 shadow-lg shadow-500/20"
      >
      <img 
      :src="profile.avatar" 
      :alt="profile.name"
      class="h-full w-full object-cover"
    </div
    ><h1>{{ profile.name }}</h1>
      <p>{{ profile.slogan }}</p>
    </div>
  </main>
</template>

