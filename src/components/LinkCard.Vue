<template>
  <a
    href="#"
    target="_blank"
    rel="noopener noreferrer"
    class="flex w-full items-center gap-4 rounded-xl border border-gray-700 bg-gray-800 p-4 shadow-md transition-all duration-300 hover:scale-[1.02]"
  >
    <!-- Icon Container -->
    <div class="flex h-12 w-12 shrink-0 items-center justify-center rounded-lg bg-gray-700">
      <svg
        viewBox="0 0 24 24"
        fill="none"
        stroke="currentColor"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
        class="h-6 w-6 text-white"
      >
        <!-- Paste your downloaded flag path data inside here -->
        <path d="M4 15s1-1 4-1 5 2 8 2 4-1 4-1V3s-1 1-4 1-5-2-8-2-4 1-4 1zM4 22v-7" />
      </svg>
    </div>

    <!-- Text Content -->
    <div class="flex flex-col">
      <span class="font-semibold text-white">Link Title</span>
      <span class="text-sm text-gray-400">Description or subtitle</span>
    </div>
  </a>
</template>
