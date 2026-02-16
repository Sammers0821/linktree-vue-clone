<script setup>
import { ref } from 'vue'
import LinkCard from '@/components/LinkCard.vue'

const profile = ref({
  name: 'Samantha Olivares',
  slogan: 'Full Time Mom and Student',
  avatar:
    'https://api.dicebear.com/9.x/adventurer/svg?backgroundType=gradientLinear&eyebrows=variant06,variant10,variant12,variant13&eyes=variant08,variant09,variant10,variant11,variant12,variant13,variant14,variant15,variant16,variant17,variant18,variant19,variant20,variant21,variant22,variant23,variant24,variant25,variant26,variant03,variant02,variant01&features=birthmark,freckles&glasses=variant02,variant04,variant05&hair=long06,long09,long16,long19&hairColor=0e0e0e,562306,6a4e35,ac6511&mouth=variant26,variant25,variant23,variant22,variant27,variant02,variant01&skinColor=ecad80&backgroundColor=ffd5dc&seed=Josylan',
})
</script>

<template>
  <main class="px flex min-h-screen flex-col items-center px-4 py-8">
    <!-- Profile Header-->
    <div class="mb-8 flex flex-col items-center text-center">
      <div
        class="border-b-amber-40 mb-4 h-24 w-24 overflow-hidden rounded-full border-4 border-cyan-300"
      >
        <img
          :src="profile.avatar"
          :alt="profile.name"
          class="h-full w-full object-cover"
        />
      </div>
      <h1 class="mb-2 font-display text-2xl font-bold text-white sm:text-3xl">
        {{ profile.name }}
      </h1>
      <p class="max-w-xs text-gray-300 sm:text-lg">{{ profile.slogan }}</p>
    </div>

    <!-- Link List -->
    <div class="flex w-full max-w-md flex-col gap-4">
      <LinkCard
        v-for="x of [1, 2, 3]"
        :key="x"
      />
    </div>

    <!-- Navigate to Info -->
    <RouterLink
      to="/info"
      class="mt-8 text-sm text-gray-200 underline-offset-4 transition-colors duration-200 hover:text-teal-300 hover:underline"
    >
      About me →
    </RouterLink>
  </main>
</template>
