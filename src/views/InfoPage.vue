<script setup>
import { ref } from 'vue'

const bio = ref({
  name: 'Samantha Olivares',
  avatar:
    'https://api.dicebear.com/9.x/adventurer/svg?backgroundType=gradientLinear&eyebrows=variant06,variant10,variant12,variant13&eyes=variant08,variant09,variant10,variant11,variant12,variant13,variant14,variant15,variant16,variant17,variant18,variant19,variant20,variant21,variant22,variant23,variant24,variant25,variant26,variant03,variant02,variant01&features=birthmark,freckles&glasses=variant02,variant04,variant05&hair=long06,long09,long16,long19&hairColor=0e0e0e,562306,6a4e35,ac6511&mouth=variant26,variant25,variant23,variant22,variant27,variant02,variant01&skinColor=ecad80&backgroundColor=ffd5dc&seed=Josylan',
  about: `I am a full time Mom and full time Student! I love to learn new things especially when it comes to being creative.`,
  skills: ['Vue.js', 'Learn', 'Typescript', 'Read', 'Crochet'],
  email: 'soliva41@stu.southtexascolleege.edu',
  location: 'Donna, Tx',
})
</script>

<template>
  <main class="flex min-h-screen flex-col items-center px-4 py-8 sm:py-12">
    <RouterLink
      to="/"
      class="my-8 self-start text-sm text-gray-400 underline-offset-4 transition-colors duration-200 hover:text-teal-400 hover:underline"
    >
      ← Back to Links
    </RouterLink>

    <!-- Profile Card -->
    <div
      class="w-full max-w-lg rounded-2xl border border-gray-700 bg-gray-800 p-6 shadow-xl shadow-gray-900/50 sm:p-8"
    >
      <!-- Header -->
      <div class="mb-6 flex flex-col items-center text-center sm:flex-row sm:text-left">
        <div
          class="mb-4 h-20 w-20 shrink-0 overflow-hidden rounded-full border-4 border-teal-400 sm:mr-6 sm:mb-0"
        >
          <img
            :src="bio.avatar"
            :alt="bio.name"
            class="h-full w-full object-cover"
          />
        </div>
        <div>
          <h1 class="mb-1 font-display text-2xl font-bold text-white">{{ bio.name }}</h1>
          <p class="text-sm text-gray-200">📍 {{ bio.location }}</p>
        </div>
      </div>

      <!-- About Section -->
      <div class="mb-6">
        <h2 class="mb-3 text-lg font-semibold text-white">About</h2>
        <p class="leading-relaxed text-gray-300">{{ bio.about }}</p>
      </div>

      <!-- Skills Section -->
      <div class="mb-6">
        <h2 class="mb-3 text-lg font-semibold text-white">Skills</h2>
        <div class="flex flex-wrap gap-2">
          <span
            v-for="skill in bio.skills"
            :key="skill"
            class="rounded-full bg-teal-300/50 px-3 py-1 text-sm text-teal-100"
          >
            {{ skill }}
          </span>
        </div>
      </div>

      <!-- Contact -->
      <div>
        <h2 class="mb-3 text-lg font-semibold text-white">Get in Touch</h2>
        <a
          :href="`mailto:${bio.email}`"
          class="group inline-flex items-center gap-2 rounded-xl bg-teal-400 px-6 py-3 font-medium text-white shadow-lg shadow-teal-500/30 transition-all duration-200 hover:scale-105 hover:bg-teal-600 hover:shadow-xl hover:shadow-teal-500/40 active:scale-95"
        >
          <svg
            data-slot="icon"
            fill="none"
            stroke-width="1.5"
            stroke="currentColor"
            viewBox="0 0 24 24"
            xmlns="http://www.w3.org/2000/svg"
            aria-hidden="true"
            class="h-5 w-5 transition-transform duration-200 group-hover:rotate-12"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M21.75 6.75v10.5a2.25 2.25 0 0 1-2.25 2.25h-15a2.25 2.25 0 0 1-2.25-2.25V6.75m19.5 0A2.25 2.25 0 0 0 19.5 4.5h-15a2.25 2.25 0 0 0-2.25 2.25m19.5 0v.243a2.25 2.25 0 0 1-1.07 1.916l-7.5 4.615a2.25 2.25 0 0 1-2.36 0L3.32 8.91a2.25 2.25 0 0 1-1.07-1.916V6.75"
            ></path>
          </svg>
          Send Email
        </a>
      </div>
    </div>
  </main>
</template>
