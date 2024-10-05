<script setup lang="ts">
import { onMounted, ref } from 'vue'

// References for countup elements
const courseCount = ref<number>(0)
const studentCount = ref<number>(0)
const visitorCount = ref<number>(0)

// Function to simulate fetching data and updating counts
function fetchDataAndUpdateCounts() {
  // Simulated data, you can replace this with actual data fetching logic
  const numberOfCourses = 50
  const numberOfStudents = 1000
  const numberOfVisitors = 50000

  // Update counts
  courseCount.value = numberOfCourses
  studentCount.value = numberOfStudents
  visitorCount.value = numberOfVisitors
}

// Fetch data and update counts on component mount
onMounted(() => {
  fetchDataAndUpdateCounts()
})
</script>

<template>
  <div class="container mx-auto mt-8">
    <div class="grid grid-cols-1 sm:grid-cols-2 items-center">
      <div class="px-6">
        <h4 class="dark:text-zinc-300 font-semibold leading-tight text-2xl md:text-2xl my-5">
          We are a non-profit organization focused on raising sustainability leaders towards a Sustainable Philippines
        </h4>
        <p class="dark:text-zinc-300">
          Championing leaders for a sustainable Philippines.
        </p>
        <ClientOnly>
          <div class="mt-4">
            <p class="dark:text-zinc-300">
              Number of Students Enrolled
              <span class="primaryColor flex font-bold text-lg md:text-xl">
                <CountUp :end-val="courseCount" />+
              </span>
            </p>
            <p class="dark:text-zinc-300">
              Total Hours of Content
              <span class="primaryColor flex font-bold text-lg md:text-xl">
                <CountUp :end-val="studentCount" />+
              </span>
            </p>
          </div>
        </ClientOnly>
      </div>

      <!-- Responsive iframe for YouTube video -->
      <div class="w-full h-64 sm:h-80 md:h-96 lg:h-[315px]">
        <iframe 
          class="w-full h-full"
          src="https://www.youtube.com/embed/ajg-cuaOOi0" 
          title="YouTube video player" 
          frameborder="0" 
          allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
          allowfullscreen>
        </iframe>
      </div>
    </div>
  </div>
</template>


