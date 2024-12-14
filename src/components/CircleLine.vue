<script setup lang="ts">
import { defineProps } from "vue";

defineProps<{
  isActive?: boolean;
}>();
</script>

<template>
  <div class="flex flex-col justify-center">
    <span
      class="size-3 border border-[#DCDCDC] rounded-full"
      :class="{ 'bg-[#DCDCDC]': isActive }"
    ></span>
  </div>
</template>
