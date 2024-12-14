<script lang="ts">
export default {
  name: "EducationItem",
};
</script>
<script setup lang="ts">
import CircleLine from "./CircleLine.vue";
import ExperienceRole from "./ExperienceRole.vue";
import { educations } from "@/config/education";
</script>
<template>
  <section class="space-y-6">
    <h1 class="font-semibold text-lg border-b-2 text-main border-main w-fit">Education</h1>
    <div class="flex flex-col gap-y-4 min-w-fit">
      <div v-for="education in educations" :key="education.id" class="flex gap-x-4 items-center">
        <p class="font-medium flex-1 text-right text-[8px] text-[#292929]">{{ education.year }}</p>
        <CircleLine :is-active="education.id === 1" />
        <ExperienceRole :role="education.degree" :company="education.institute" />
      </div>
    </div>
  </section>
</template>
