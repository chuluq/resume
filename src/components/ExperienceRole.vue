<script setup lang="ts">
import { defineProps } from "vue";

defineProps<{
  role: string;
  company: string;
}>();
</script>

<template>
  <div class="flex flex-col flex-1">
    <p class="font-bold text-[8px] text-[#292929]">{{ role }}</p>
    <p class="font-medium text-[8px] text-[#292929]">{{ company }}</p>
  </div>
</template>
