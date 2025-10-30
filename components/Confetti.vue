<script setup lang="ts">
import { onMounted, useTemplateRef, ref } from 'vue'
import confetti from 'canvas-confetti'

const NUMBER_OF_POPS = 5

const canvasRef = useTemplateRef<HTMLCanvasElement>('canvasRef')
const countOfPops = ref(NUMBER_OF_POPS)

function randomInRange(min: number, max: number): number {
  return Math.random() * (max - min) + min
}

onMounted(() => {
  if (!canvasRef.value) return

  const myConfetti = confetti.create(canvasRef.value, { resize: true }) as any
  const pumpkin = confetti.shapeFromText({ text: '🎃' });
  const zombie = confetti.shapeFromText({ text: '🧟‍♀️' });
  const canddy = confetti.shapeFromText({ text: '🍬' });
  const web = confetti.shapeFromText({ text: '🕸️' });

  const intervalId = setInterval(() => {
    if (countOfPops.value <= 0) {
      clearInterval(intervalId);
      return
    }
    myConfetti({
      shapes: [pumpkin, zombie, canddy, web],
      angle: randomInRange(80, 100),
      spread: randomInRange(60, 120),
      particleCount: randomInRange(100, 300),
      origin: { y: 1 },
      gravity: randomInRange(0.1, 1.6),
      scalar: randomInRange(0.6, 1.2),
    })

    countOfPops.value -= 1
  }, Math.random() * 10 + 200)
})
</script>

<template>
  <div class="absolute inset-0 overflow-hidden pointer-events-none">
    <canvas ref="canvasRef" class="w-full h-full text-9xl"></canvas>
  </div>
</template>
