<script setup lang="ts">
const open = ref(false)
</script>

<template>
  <div class="group absolute right-2 top-1/2 cursor-pointer rounded-full bg-white p-3 shadow transition-transform duration-150 active:scale-90 hover:scale-110" @click="open = true">
    <div class="i-mdi-settings transition-transform duration-1000 group-hover:rotate-180" />
  </div>
  <NDialog v-model:open="open">
    <HelloWorld msg="Vite + Vue" />
  </NDialog>
</template>
