<script setup lang="ts">
defineProps<{
  title: string
  imgSrc?: string
  link?: string
  flavorText?: string
}>()
</script>

<template>
  <div class="flex flex-col gap-4">
    <h2 class="text-lg font-bold"> {{ title }}</h2>
    <div v-if="imgSrc" class="flex justify-center md:justify-start">
      <img :src="imgSrc" class="w-[500px] border-8 border-white shadow-md" />
    </div>
    <p>
      <slot></slot>
    </p>
    <slot name="tech-stack"></slot>
    <p v-if="flavorText" class="italic text-gray-500 border-l-4 pl-2">
      {{ flavorText }}
      <br class="sm:hidden" />
      <a v-if="link" :href="link" target=”_blank”>{{ link }}</a>
    </p>
  </div>
</template>