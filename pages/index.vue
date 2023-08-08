<script setup>
  
useHead({
  title: 'Home',
  script: [
    { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
  ]
});

</script>
<template>
  <main class="mx-auto max-w-4xl space-y-6">
    <h1 class="text-4xl">Welcome!</h1>
    <hr>
    <div class="space-y-4 mb">
      <p>This template demonstrates the creation of a static site using:</p>
      <ul class="list-disc list-inside">
        <li>Nuxt 3</li>
        <li>Tailwind CSS</li>
        <li>Decap CMS (formerly Netlify)</li>
      </ul>
    </div>
    <div>
      <h2 class="text-2xl">The Blog</h2>
      <p>The blog is the core of this site. <NuxtLink to="/blog" class="underline text-indigo-300">Click here -></NuxtLink></p>
    </div>
  </main>
</template>