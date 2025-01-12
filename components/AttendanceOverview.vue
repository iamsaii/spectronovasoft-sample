<template>
  <div class="bg-white p-6 rounded-lg shadow-sm">
    <div class="flex justify-between items-center mb-6">
      <h3 class="font-medium text-gray-900">Attendance Overview</h3>
      <div class="flex items-center space-x-2">
        <span class="text-4xl font-semibold">{{ percentage }}%</span>
        <span class="text-green-500 text-sm">{{ improvement }} since last month</span>
      </div>
    </div>

    <div class="relative h-3 w-full rounded-full overflow-hidden bg-gray-100">
      <div
        class="absolute left-0 top-0 h-full bg-purple-500 transition-all duration-300"
        :style="{ width: `${onTimePercentage}%` }"
      />
      <div
        class="absolute left-0 top-0 h-full bg-blue-400 transition-all duration-300"
        :style="{ width: `${dayOffPercentage}%` }"
      />
      <div
        class="absolute left-0 top-0 h-full bg-yellow-400 transition-all duration-300"
        :style="{ width: `${sickLeavePercentage}%` }"
      />
    </div>

    <div class="flex items-center space-x-6 mt-4">
      <div class="flex items-center space-x-2">
        <div class="w-3 h-3 rounded-full bg-yellow-400" />
        <span class="text-sm text-gray-600">Sick Leave</span>
      </div>
      <div class="flex items-center space-x-2">
        <div class="w-3 h-3 rounded-full bg-blue-400" />
        <span class="text-sm text-gray-600">Day Off</span>
      </div>
      <div class="flex items-center space-x-2">
        <div class="w-3 h-3 rounded-full bg-purple-500" />
        <span class="text-sm text-gray-600">On time</span>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  percentage: {
    type: Number,
    default: 90,
  },
  improvement: {
    type: String,
    default: '+20%',
  },
  onTimePercentage: {
    type: Number,
    default: 60,
  },
  dayOffPercentage: {
    type: Number,
    default: 25,
  },
  sickLeavePercentage: {
    type: Number,
    default: 5,
  },
})
</script>
