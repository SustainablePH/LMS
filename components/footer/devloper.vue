<script setup lang="ts">


</script>

<template>
  <div>
    <p class=" dark:text-zinc-300   text-l py-1 font-semibold">
      We are a volunteer-led organization, with our work made possible through passionate leaders who believe in our cause.

Help us continue our mission to raise more sustainability leaders.
    </p>
    <a
      href="https://sustainableph.org/donate/"
      class="block text-center w-full bg-sky-700 p-2 rounded-lg text-[#F1F2F4]  mt-3 text-sm"
    >
     Donate
    </a>
    <div class="my-3 space-x-3 pb-3">

      <NuxtLink
        to="https://www.linkedin.com/company/sustainableph/"
        target="_blank"
        class="p-2 bg-gray-300 text-gray-800 rounded-md dark:bg-sky-700 dark:text-[#F1F2F4]"
        aria-label="LinkedIn"
      >
        <Icon name="fa:linkedin-square" size="1em" />
      </NuxtLink>
      <NuxtLink
        to="https://www.youtube.com/c/sustainablephtv"
        target="_blank"
        class="p-2 bg-gray-300 text-gray-800 rounded-md dark:bg-sky-700 dark:text-[#F1F2F4]"
        aria-label="Youtube"
      >
        <Icon name="fa:youtube-square" size="1em" />
      </NuxtLink>
      <NuxtLink
        to="https://www.facebook.com/sustainablephofficial"
        target="_blank"
        class="p-2 bg-gray-300 text-gray-800 rounded-md dark:bg-sky-700 dark:text-[#F1F2F4]"
        aria-label="StackOverflow"
      >
        <Icon name="ri:facebook-fill" size="1em" />
      </NuxtLink>
    </div>
  </div>
</template>
