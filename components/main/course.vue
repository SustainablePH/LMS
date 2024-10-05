<script lang="ts" setup>
// Get Last 6 Publish Post from the content/blog directory

useHead({
  title: 'Home',
  meta: [
    {
      name: 'description',
      content:
        'Welcome to SustainablePh We are a non-profit organization focused on raising sustainability leaders towards a Sustainable Philippines',
    },
  ],
  titleTemplate: 'SustainablePh - %s',
})

const data: string[] = []


</script>

<template>
  <div class="pb-10 px-4">
    <div class="flex flex-row items-center space-x-3 pt-5 pb-3">
      <Icon name="mdi:book" size="2em" class=" dark:text-zinc-300" />
      <h2 class="text-4xl font-semibold  dark:text-zinc-300   ">
        Our Courses
      </h2>
    </div>

    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">


      <template v-if="data?.length === 0">
        <BlogEmpty />
      </template>
    </div>
  </div>
</template>
