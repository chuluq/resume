<script lang="ts">
export default {
  name: "SidebarItem",
};
</script>
<script setup lang="ts">
import { personalData, skills } from "@/config/personal-info";
</script>

<template>
  <aside class="w-[190px] h-full flex flex-col gap-y-6 shadow-lg pb-4">
    <div class="size-[190px]">
      <img src="../assets/img/profile.png" alt="profile" />
    </div>
    <div class="px-[27.5px] flex flex-col gap-y-8">
      <section class="text-center space-y-2">
        <div v-for="item in personalData" :key="item.id">
          <h3 class="font-bold text-[10px] leading-[15px] text-[#292929]">{{ item.label }}</h3>
          <h3 class="font-medium text-[10px] leading-[15px] text-[#292929]">{{ item.data }}</h3>
        </div>
      </section>
      <section class="gap-y-4 flex flex-col items-center justify-center">
        <h1 class="font-semibold text-lg border-b-2 text-[#292929] border-[#292929]">Languages</h1>
        <div class="space-y-1 text-center">
          <h3 class="font-medium text-[10px] leading-[15px] text-[#292929]">Indonesia</h3>
          <h3 class="font-medium text-[10px] leading-[15px] text-[#292929]">English</h3>
        </div>
      </section>
      <section class="gap-y-4 flex flex-col items-center justify-center">
        <h1 class="font-semibold text-lg border-b-2 text-[#292929] border-[#292929]">Skills</h1>
        <div class="space-y-1 text-center">
          <h3
            v-for="skill in skills"
            :key="skill.id"
            class="font-medium text-[10px] leading-[15px] text-[#292929]"
          >
            {{ skill.data }}
          </h3>
        </div>
      </section>
    </div>
  </aside>
</template>
