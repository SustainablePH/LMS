<script setup lang="ts">
import { ref } from 'vue'

const supabase = useSupabaseClient()

const username = ref('')
const email = ref('')
const password = ref('')
const confirmPassword = ref('')
const phoneNumber = ref('')
const errorMessage = ref('')

const passwordVisible = ref(false)
const confirmPasswordVisible = ref(false)
const showErrorMessage = ref(false)
const isFetching = ref(false)

function toggleVisibility(inputId: string) {
  if (inputId === 'password')
    passwordVisible.value = !passwordVisible.value
  else if (inputId === 'confirmPassword')
    confirmPasswordVisible.value = !confirmPasswordVisible.value
}

async function handleSubmit() {
    try {
        const { data, error } = await supabase.auth.signInWithPassword({
  email: email.value,
  password: password.value,
})

navigateTo('/')

      
    } catch (error) {
        console.log(error)
    }
}
</script>

<template>
  <section class="dark:bg-gray-900 min-h-screen flex items-center justify-center">
    <!-- লগইন কন্টেনার -->
    <div class="dark:bg-gray-800 flex rounded-2xl shadow-lg max-w-6xl p-5 items-center">
      <!-- ফর্ম -->
      <div class="w-full px-8">
        <h2 class="font-bold text-2xl text-[#002D74] dark:text-zinc-400">
         SignIn
        </h2>
        <p class="text-s mt-4 text-[#002D74] dark:text-gray-300">
        SignupData
        </p>
        <p v-if="showErrorMessage" style="color: red;">
          Error: {{ errorMessage }}
        </p>
        <form class="flex flex-col gap-4">
          
          <input v-model="email" class="p-2 rounded-xl border bg-white dark:bg-gray-600 text-[#002D74] dark:text-gray-300" type="email" name="email" placeholder="Email">
          <div class="relative">
            <input v-model="password" class="p-2 rounded-xl border w-full bg-white dark:bg-gray-600 text-[#002D74] dark:text-gray-300" :type="passwordVisible ? 'text' : 'password'" name="password" placeholder="Password">
            <Icon :name="passwordVisible ? 'mdi:eye' : 'mdi:eye-off'" color="black" class="absolute top-1/2 -translate-y-1/2 right-4 cursor-pointer" @click="toggleVisibility('password')" />
          </div>
          <button type="submit" class="bg-sky-700 rounded-xl text-white py-2 hover:scale-105 duration-300" @click.prevent="handleSubmit">
            <span v-if="isFetching" class="flex items-center justify-center">
              <div class="spinner" />
            </span>
            <span v-else>
            Login
            </span>
          </button>
        </form>

        <div class="mt-3 text-xs flex justify-between items-center text-[#002D74] dark:text-gray-300">
          <p>Don't Have an Account</p>
          <NuxtLink to="/signup" aria-label="লগইন" class="ml-2 mr-2">
            <button class="py-2 px-5 bg-white border text-[#002D74] rounded-xl hover:scale-110 duration-300">
              SignUp
            </button>
          </NuxtLink>
        </div>
      </div>
    </div>
  </section>
</template>