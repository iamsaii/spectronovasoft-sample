<template>
  <div class="bg-white p-6 rounded-lg shadow-sm">
    <div class="flex justify-between items-center mb-6">
      <div>
        <h3 class="font-medium text-gray-900">Employee Performance Ratings</h3>
        <div class="flex items-baseline mt-2">
          <span class="text-3xl font-bold">{{ overallPerformance }}%</span>
          <p class="text-sm text-gray-500 ml-2">
            At Tur Agency, we're proud of our employees' consistent punctuality and quality work.
          </p>
        </div>
      </div>
      <button class="text-gray-400 hover:text-gray-600">
        <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z" />
        </svg>
      </button>
    </div>

    <div class="flex gap-4 mb-6">
      <div v-for="metric in metrics" :key="metric.name" class="flex items-center gap-2">
        <div class="w-3 h-3 rounded-full" :class="metric.color" />
        <span class="text-sm text-gray-600">{{ metric.name }}</span>
      </div>
    </div>

    <div class="space-y-6">
      <div v-for="employee in employees" :key="employee.name">
        <div class="flex justify-between items-center">
          <span class="text-sm text-gray-600">{{ employee.name }}</span>
          <span class="text-sm text-gray-400">{{ getTotalScore(employee) }}</span>
        </div>
        <div class="flex items-center gap-2 mt-2">
          <div 
            v-for="(metric, index) in metrics" 
            :key="index"
            class="h-2 rounded-full transition-all duration-300"
            :class="metric.color"
            :style="{ width: getWidth(employee[metric.key]) }"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  overallPerformance: {
    type: Number,
    default: 98
  }
})

const maxValue = 40 

const metrics = ref([
  { name: 'Task completed', key: 'tasks', color: 'bg-purple-500' },
  { name: 'Presence', key: 'presence', color: 'bg-blue-400' },
  { name: 'Completed Meeting', key: 'meetings', color: 'bg-teal-500' }
])

const employees = ref([
  {
    name: 'Ahsan Tapadar',
    tasks: 15,
    presence: 12,
    meetings: 8
  },
  {
    name: 'Koyes Ahmed',
    tasks: 18,
    presence: 10,
    meetings: 7
  },
  {
    name: 'Washi Bin M.',
    tasks: 25,
    presence: 8,
    meetings: 5
  },
  {
    name: 'Mir Muhsin',
    tasks: 12,
    presence: 15,
    meetings: 10
  },
  {
    name: 'Turja Sen Das',
    tasks: 20,
    presence: 10,
    meetings: 8
  }
])

const getWidth = (value) => `${(value / maxValue) * 100}%`

const getTotalScore = (employee) => {
  return employee.tasks + employee.presence + employee.meetings
}
</script>