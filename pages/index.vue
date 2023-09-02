<script lang="ts" setup>
useHead({
  title: 'Home',
  meta: [
    {
      name: 'description',
      content:
      'Welcome To My Blog Site. Get API Design, API Security, Golang and System Design, Related Articles,Tips, Learning Resources and More.',
    },
  ],
  titleTemplate: 'Sang Dennis - %s',
})
</script>

<template>
  <main class="container max-w-5xl mx-auto text-zinc-600">
    <MainHero />
    <MainRecent />
    <MainTrending />
  </main>
</template>
