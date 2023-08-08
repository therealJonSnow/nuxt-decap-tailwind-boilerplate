<template>
  <main class="mx-auto max-w-4xl space-y-6">
    <h1 class="text-4xl">The Blog</h1>
    <hr>
    <ul class="list-disc list-inside">
      <li v-for="post of posts" :key="post.slug">
        <NuxtLink :to="post._path">{{ post.title }}</NuxtLink>
      </li>
    </ul>
  </main>
</template>

<script setup>
const { data: posts } = await useAsyncData('posts', () => {
  return queryContent('/blog').find()
})
</script>