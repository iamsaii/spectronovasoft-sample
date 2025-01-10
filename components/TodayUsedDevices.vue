<template>
  <div class="bg-white p-6 rounded-lg shadow-sm">
    <div class="flex justify-between items-center mb-6">
      <h3 class="font-medium text-gray-900">Today Used Devices</h3>
      <button class="text-gray-400 hover:text-gray-600">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z" />
        </svg>
      </button>
    </div>

    <!-- Gauge Chart Component -->
    <div class="relative w-32 h-16 mx-auto">
      <!-- Background Arc -->
      <div class="absolute w-full h-full">
        <svg viewBox="0 0 100 50" class="w-full h-full">
          <path
            d="M 10 45 A 35 35 0 0 1 90 45"
            fill="none"
            stroke="#e5e7eb"
            stroke-width="8"
            stroke-linecap="round"
          />
        </svg>
      </div>
      
      <!-- Foreground Arc -->
      <div class="absolute w-full h-full" :style="{ transform: `rotate(${-90}deg)` }">
        <svg viewBox="0 0 100 50" class="w-full h-full">
          <path
            d="M 10 45 A 35 35 0 0 1 90 45"
            fill="none"
            stroke="#8b5cf6"
            stroke-width="8"
            stroke-linecap="round"
            stroke-dasharray="126"
            :stroke-dashoffset="126 - (126 * value / 100)"
            transform="rotate(180, 50, 45)"
          />
        </svg>
      </div>
      
      <!-- Center Value -->
      <div class="absolute inset-0 flex items-center justify-center mt-4">
        <span class="text-2xl font-semibold">{{ value }}</span>
      </div>
      
      <!-- Overall Label -->
      <div class="absolute -bottom-2 left-1/2 transform -translate-x-1/2">
        <span class="text-sm text-gray-500">Overall</span>
      </div>
    </div>

    <!-- Devices List -->
    <div class="mt-6 space-y-3">
      <div v-for="device in devices" :key="device.name" class="flex items-center justify-between">
        <div class="flex items-center space-x-2">
          <div :class="['w-2 h-2 rounded-full', device.color]" />
          <span class="text-sm text-gray-600">{{ device.name }}</span>
        </div>
        <span class="text-sm font-medium">{{ device.count }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  value: {
    type: Number,
    default: 100
  }
})

const devices = ref([
  { name: 'Macbook', count: 80, color: 'bg-blue-500' },
  { name: 'Keyboard', count: 13, color: 'bg-yellow-500' },
  { name: 'Headphones', count: 7, color: 'bg-purple-500' }
])
</script>