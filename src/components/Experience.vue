<script lang="ts">
export default {
  name: "ExperienceItem",
};
</script>
<script setup lang="ts">
import { experiences } from "@/config/experience";
import CircleLine from "./CircleLine.vue";
import ExperienceDate from "./ExperienceDate.vue";
import ExperienceRole from "./ExperienceRole.vue";
</script>
<template>
  <section class="space-y-6">
    <h1 class="font-semibold text-lg border-b-2 text-main border-main w-fit">Experience</h1>
    <div class="flex flex-col gap-y-4 min-w-fit">
      <div v-for="experience in experiences" :key="experience.id" class="flex gap-x-4">
        <ExperienceDate :time="experience.timeline" :place="experience.place" />
        <CircleLine :is-active="experience.id === 1" />
        <ExperienceRole :role="experience.role" :company="experience.company" />
      </div>
    </div>
  </section>
</template>
