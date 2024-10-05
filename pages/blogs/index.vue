<template>
  <div class="dark:bg-slate-950 min-h-screen w-full mt-10">
    <main class="text-zinc-600 max-w-6xl mx-auto">
      <h1 class="text-2xl font-bold mb-4 px-6">Blog Posts</h1>
      
      <div v-if="blogs.length > 0" class="px-6">
        <ul>
          <li v-for="blog in blogs" :key="blog.path" class="mb-4">
            <NuxtLink :to="blog.path" class="text-blue-600 hover:underline">
              {{ blog.title }}
            </NuxtLink>
            <p class="text-sm text-gray-500">{{ blog.date }}</p>
          </li>
        </ul>
      </div>
      <p v-else class="px-6">No blog posts available at the moment.</p>
    </main>
  </div>
</template>

<script setup>
// For demonstration purposes, we're using an empty array
// In a real scenario, you'd fetch this data from your content source
const blogs = ref([])

useHead({
  title: 'Blog Posts',
  meta: [
    {
      name: 'description',
      content: 'List of all blog posts.',
    },
  ],
  titleTemplate: 'SustainablePH',
})
</script>