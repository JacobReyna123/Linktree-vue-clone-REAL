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
    <div>
      <img :src="profile.avatar" :alt="profile.name">
      <h1>{{ profile.name }}</h1>
      <p>{{ profile.slogan }}</p>
    </div>
  </main>
</template>

