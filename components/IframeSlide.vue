<script setup lang="ts">
defineProps<{
  url: string
}>()
</script>

<template>
  <div class="absolute inset-0">
    <iframe
      :src="url"
      class="iframe-fullscreen"
      frameborder="0"
      loading="lazy"
    ></iframe>
  </div>
</template>

<style scoped>
.iframe-fullscreen {
  width: 100%;
  height: 100%;
  border: none;
}

.iframe-fullscreen::-webkit-scrollbar {
  display: none;
}

.iframe-fullscreen {
  -ms-overflow-style: none;
  scrollbar-width: none;
}
</style>
