<template>
    <main class="mx-auto max-w-4xl space-y-6">
    <NuxtLink to="/blog">&lt; Back</NuxtLink>
    <h1 class="text-4xl">
      {{ post.title }}
    </h1>
    <p>{{ post.description }}</p>
    <hr>
    <ContentDoc />
  </main>
</template>

<script setup>
const route = useRoute()

const actualPath = route.path.replace(/\/$/, '');

const { data: post } = await useAsyncData(`hello`, () =>
    queryContent(actualPath).findOne()
);
</script>