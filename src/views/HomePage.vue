<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Jacob Reyna',
  slogan: 'Game Designer in the Making',
  avatar: new URL('@/assets/Profile.jpeg', import.meta.url).href,
  links: [
    {
      id: 1,
      title: 'Github', 
      url: 'https://github.com',
      icon: 'computer',
      description: 'Check out my Github'
    },
    {
        id: 2,
      title: 'Indeed', 
      url: 'https://indeed.com',
      icon: 'briefcase',
      description: 'Preview my Job Skills'
    },
    {
      id: 3,
      title: 'SPLIT-O-MATIC',
      url: 'https://expense-splitter-vue.thecomicclan.workers.dev/',
      icon: 'code',
      description: 'Live Vue web application project'
    }
  ]
})
</script>


<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8">
    <!--Profile Header-->
    <div class="mb-8 flex flex-col items-center text-center">
       <div class="mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-green-400 shadow-lg shadow-green-500/20 sm:h-32 sm:w-32">
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="font-display mb-2 text-2xl font-bold text-white sm:text-3xl">{{ profile.name }}</h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!--LINK LIST-->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard 
        v-for="link in profile.links"
        :key="link.id"
        :link="link"
        :title="link.title"
        :url="link.url"
        :description="link.description"
        :icon="link.icon"
      />
    </div>

    <!--NAVIGATE TO INFO-->
    <RouterLink to="/info"
     class="mt-8 text-gray-400 underline-offset-4 hover:text-green-400 hover:underline transition-colors duration-200"
    >About Link ➡️</RouterLink>
  </main>
</template>


