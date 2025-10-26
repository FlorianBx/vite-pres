<script setup lang="ts">
</script>

<template>
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <div class="pulse-gradient-blue"></div>
    <div class="pulse-gradient-violet"></div>
  </div>
</template>

<style scoped>
@keyframes pulse-fade {
  0% {
    opacity: 0.1;
    transform: scale(1);
  }
  25% {
    opacity: 0.3;
    transform: scale(1.1);
  }
  50% {
    opacity: 0.2;
    transform: scale(0.95);
  }
  75% {
    opacity: 0.25;
    transform: scale(1.05);
  }
  85% {
    opacity: 0.2;
    transform: scale(1);
  }
  100% {
    opacity: 0;
    transform: scale(1);
  }
}

.pulse-gradient-blue {
  position: absolute;
  top: -20%;
  right: -10%;
  width: 600px;
  height: 600px;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.5), transparent 70%);
  animation: pulse-fade 3s ease-in-out forwards;
  border-radius: 50%;
}

.pulse-gradient-violet {
  position: absolute;
  bottom: -20%;
  left: -10%;
  width: 700px;
  height: 700px;
  background: radial-gradient(circle, rgba(139, 92, 246, 0.5), transparent 70%);
  animation: pulse-fade 3s ease-in-out forwards;
  animation-delay: 0.3s;
  border-radius: 50%;
}
</style>
