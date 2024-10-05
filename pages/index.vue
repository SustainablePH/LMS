<script lang="ts" setup>
useHead({
  title: 'Home',
  meta: [
    {
      name: 'description',
      content:
        'Championing leaders for a sustainable Philippines.',
    },
  ],
  titleTemplate: 'Sustainable  - %s',
})


</script>

<template>
  <div class="dark:bg-slate-950 min-h-screen">
    <main class="container max-w-6xl mx-auto text-zinc-600">
    
      <MainHero />
      <MainCourse />
      <MainBlogs />
    </main>
  </div>
</template>
