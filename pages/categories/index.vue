<script lang="ts" setup>
import { makeFirstCharUpper } from '@/utils/helper'

const topics = [
  'golang',
  'Elixir',
  'API Design',
  'API Security',
  'docker',
  'kubernetes',
  'Design Patterns',
  'System Design',
]

useHead({
  title: 'Categories',
  meta: [
    {
      name: 'description',
      content:
        'Listed below are all the topics which either I have written a blog post about or will write about in the near future.',
    },
  ],
  titleTemplate: 'Sang Dennis - %s',
})
</script>

<template>
  <main class="container max-w-5xl mx-auto text-zinc-600">
    <CategoryHero />
    <div class="flex flex-wrap px-6 mt-12 gap-3">
      <template v-for="topic in topics" :key="topic">
        <CategoryCard :title="makeFirstCharUpper(topic)" />
      </template>
    </div>
  </main>
</template>
