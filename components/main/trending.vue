<script lang="ts" setup>
// Get Last 6 Publish Post from the content/blog directory
const { data } = await useAsyncData('trending-post', () =>
  queryContent('/blogs').limit(3).sort({ _id: 1 }).find(),
)

const formatedData = computed(() => {
  return data.value?.map((articles) => {
    return {
      path: articles._path,
      title: articles.title || 'no-title available',
      description: articles.description || 'no-descriptoin available',
      image: articles.image || '/nuxt-blog/no-image_cyyits.png',
      alt: articles.alt || 'no alter data available',
      ogImage: articles.ogImage || '/nuxt-blog/no-image_cyyits.png',
      date: articles.date || 'not-date-available',
      tags: articles.tags || [],
      published: articles.published || false,
    }
  })
})

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
  <div>
    <div class="px-6">
      <div class="flex flex-row items-center space-x-3 pt-5 pb-3">
        <Icon name="mdi:star-three-points-outline" size="2em" class="text-black" />
        <h2 class="text-4xl font-semibold text-black ">
          Trending Post
        </h2>
      </div>
    </div>
    <div class="grid grid-cols-1 ">
      <template v-for="post in formatedData" :key="post.title">
        <ArchiveCard
          :path="post.path"
          :title="post.title"
          :date="post.date"
          :description="post.description"
          :image="post.image"
          :alt="post.alt"
          :og-image="post.ogImage"
          :tags="post.tags"
          :published="post.published"
        />
      </template>
      <template v-if="data?.length === 0">
        <BlogEmpty />
      </template>
    </div>
  </div>
</template>
