<template>
  <div>
    <VitePwaManifest />
    <NuxtPage />
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Unbounded&display=swap');
</style>

<!-- <script setup>
// If you want to use it in setup, import from the nuxtApp.
const { $pwa } = useNuxtApp()

const toast = useToast()
onMounted(() => {
  if ($pwa.offlineReady) {
    toast.success('App ready to work offline')
  }
})
</script> -->

<!-- <template>
  <div v-show="$pwa.needRefresh">
    <span>
      New content available, click on reload button to update.
    </span>

    <button @click="$pwa.updateServiceWorker()">
      Reload
    </button>
  </div>
</template> -->
