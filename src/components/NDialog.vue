<script setup lang="ts">
const open = defineModel<boolean>('open')
const dialog = ref()

onClickOutside(dialog, () => {
  open.value = false
})
</script>

<template>
  <div
    v-if="open"

    class="fixed inset-0 bottom-0 left-0 right-0 top-0 z-20 h-screen w-full flex flex-col items-center justify-center border bg-white/90 backdrop-blur-sm dark:bg-black/90"
  >
    <section ref="dialog" class="max-w-md w-full border border-gray rounded-xl border-solid bg-white/5 p-6 backdrop-blur-2xl">
      <slot />

      <div class="absolute right-2 top-2 flex items-center justify-center">
        <div class="i-mdi-close" @click="open = false" />
      </div>
    </section>
  </div>
</template>

<style scoped>

</style>
