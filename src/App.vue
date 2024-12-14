<script setup lang="ts">
import Education from "./components/Education.vue";
import Experience from "./components/Experience.vue";
import Intro from "./components/Intro.vue";
import Sidebar from "./components/Sidebar.vue";
</script>

<template>
  <div class="container mx-auto max-w-[595px] flex gap-x-2">
    <Sidebar />
    <main class="py-10 px-6 flex flex-col gap-y-10">
      <Intro />
      <Experience />
      <Education />
    </main>
  </div>
</template>
