<script setup lang="ts">
import { defineProps } from "vue";

defineProps<{
  time: string;
  place: string;
}>();
</script>

<template>
  <div class="flex flex-col items-end flex-1 justify-end">
    <p class="font-medium text-[8px] text-[#292929]">{{ time }}</p>
    <p class="font-medium text-[8px] text-[#292929]">{{ place }}</p>
  </div>
</template>
