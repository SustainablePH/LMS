<script setup lang="ts">
import Dogpow from '~/components/logo/dogpow.vue'


</script>

<template>
  <div class="dark:bg-slate-950 min-h-screen">
    <div class="py-5 mt-8">
      <div class="sm:grid grid-cols-8 px-6 py-5 sm:py-9 gap-5 container max-w-6xl mx-auto">
        <div class="col-span-5 max-w-md">
          <div class="flex justify-between">
            <div>
              <h1 class="dark:text-zinc-300 font-semibold leading-tight text-4xl md:text-6xl my-5">
                We are a community of volunteers that believe in a Sustainable Philippines we dream of!
              </h1>

              <div class="my-3 space-x-2 md:space-x-3 pb-10">
                <NuxtLink
                  to="https://www.linkedin.com/company/sustainableph/" target="_blank"
                  class="p-2 bg-gray-300 text-gray-800 rounded-md dark:bg-sky-700 dark:text-[#F1F2F4]"
                  aria-label="LinkedIn"
                >
                  <Icon name="fa:linkedin-square" size="1em" />
                </NuxtLink>
                <NuxtLink
                  to="https://www.youtube.com/c/sustainablephtv" target="_blank"
                  class="p-2 bg-gray-300 text-gray-800 rounded-md dark:bg-sky-700 dark:text-[#F1F2F4]"
                  aria-label="Youtube"
                >
                  <Icon name="fa:youtube-square" size="1em" />
                </NuxtLink>
                <NuxtLink
                  to="https://www.facebook.com/sustainablephofficial" target="_blank"
                  class="p-2 bg-gray-300 text-gray-800 rounded-md dark:bg-sky-700 dark:text-[#F1F2F4]"
                  aria-label="StackOverflow"
                >
                  <Icon name="ri:facebook-fill" size="1em" />
                </NuxtLink>
              </div>
            </div>
          </div>
        </div>
        <div class="hidden sm:block col-span-3">
          <Dogpow />
        </div>
      </div>

      <!-- Volunteer Images Section -->
      <div class="container mx-auto mt-8">
        <h2 class="text-2xl font-bold text-center dark:text-[#F1F2F4]">
          Meet Our Volunteers
        </h2>
        <div class="grid grid-cols-2 sm:grid-cols-4 gap-4 mt-6">
          <NuxtImg
            v-for="i in 4" :key="i" :src="`/volunteers/volunteer${i}.jpeg`" height="300" alt="Volunteer"
            class="w-full h-90 object-cover rounded-lg"
          />
        </div>
      </div>
    </div>
  </div>
</template>
