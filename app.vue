<template>
  <div class="h-screen w-screen overflow-y-auto py-10 text-slate-200 bg-slate-900">
    <NuxtPage />
  </div>
</template>

<script setup>
useHead({
  title: 'NDT Stack',
  meta: [
    { name: 'description', content: 'My amazing site.' }
  ],
  htmlAttrs: {
    lang: 'en'
  }
})
</script>