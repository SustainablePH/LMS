<script setup lang="ts">
</script>

<template>
  <div class="flex flex-col dark:text-zinc-300   my-5 md:my-0 md:justify-self-center">
    <p class=" dark:text-zinc-300  text-base font-semibold">
      Link
    </p>
    <NuxtLink to="/" class="hover:underline">
      Home
    </NuxtLink>
    <NuxtLink to="/about" class="hover:underline">
      About
    </NuxtLink>
  </div>
</template>
