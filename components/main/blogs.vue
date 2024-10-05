<script lang="ts" setup>
import { useRouter } from '#vue-router';
// Get Last 6 Publish Post from the content/blog directory

const router=useRouter()

const formattedData: string[] = []
const data: string[] = []

useHead({
  title: 'Home',
  meta: [
    {
      name: 'description',
      content:
        'Learn about all the methods , partners & challenges on Sustainability',
    },
  ],
  titleTemplate: 'SustainablePh',
})
function gotoBlogs(){
  router.push('/blogs')
}
</script>

<template>
  <div class="px-4">
    <div class="flex flex-row items-center space-x-3 pt-5 pb-3">
      <Icon name="mdi:star-three-points-outline" size="2em" class=" dark:text-zinc-300  " />
     <div class="flex ">
      <h2 class="text-4xl font-semibold  dark:text-zinc-300  ">
        Blog Posts
      </h2>
    </div> 

    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
      
      <template v-if="data?.length === 0">
        <BlogEmpty />
      </template>
    </div>
    <div class="flex justify-end mt-3">
  <button @click="gotoBlogs" class="block text-center w-full bg-sky-700 p-2 rounded-lg text-[#F1F2F4]  mt-3 text-sm">
    All Blogs
  </button>
</div>
  </div>
</template>
