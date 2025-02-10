<template>
  <NuxtLink :to="linkRoute"
    class="px-4 py-2 bg-blue-500 text-white rounded hover:bg-blue-600 transition duration-300 ease-in-out">
    {{ text }}
  </NuxtLink>
</template>

<script setup lang="ts">
import { defineProps, computed } from 'vue';

type Props = {
  linkTo: string,
  text: string
}

const props = defineProps<Props>()

const linkRoute = computed(() => `/${props.text}`)
</script>