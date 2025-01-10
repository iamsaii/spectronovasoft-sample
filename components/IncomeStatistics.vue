<template>
  <div class="bg-white p-6 rounded-lg shadow-sm">
    <div class="flex justify-between items-center mb-4">
      <h3 class="font-medium text-gray-900">Income Statistics</h3>
      <button class="text-purple-600 hover:text-purple-700 text-sm font-medium">
        Advance Filter
      </button>
    </div>

    <!-- Current Month Stats -->
    <div class="mb-6 flex items-center gap-4">
      <div class="flex items-center gap-2">
        <div class="w-8 h-8 rounded-full bg-gray-100 flex items-center justify-center">
          <svg class="w-4 h-4 text-purple-600" viewBox="0 0 24 24" fill="none" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4l3 3m6-3a9 9 0 11-18 0 9 9 0 0118 0z" />
          </svg>
        </div>
        <div>
          <p class="text-sm text-gray-500">{{ selectedMonth.month }}</p>
          <div class="flex gap-6">
            <div class="flex items-center gap-2">
              <span class="text-sm font-medium text-purple-600">Income</span>
              <span class="text-sm text-gray-900">{{ selectedMonth.income }}</span>
            </div>
            <div class="flex items-center gap-2">
              <span class="text-sm font-medium text-blue-400">Expense</span>
              <span class="text-sm text-gray-900">{{ selectedMonth.expense }}</span>
            </div>
          </div>
        </div>
      </div>
    </div>

    <!-- Chart -->
    <div class="h-64">
      <VueApexCharts
        type="bar"
        height="100%"
        :options="chartOptions"
        :series="series"
      />
    </div>
  </div>
</template>

<script setup>
const selectedMonth = ref({
  month: 'May 2024',
  income: '$2198.11',
  expense: '$733.43'
})

const series = ref([
  {
    name: 'Expense',
    data: [2000, 2500, 3000, 4000, 4500, 3500, 4000, 3200, 3800, 3400, 3000, 2800]
  },
  {
    name: 'Income',
    data: [3000, 4000, 5000, 7000, 8000, 6000, 7000, 5500, 6500, 5800, 5000, 4500]
  }
])

const chartOptions = ref({
  chart: {
    type: 'bar',
    stacked: true,
    stackType: '100%',
    toolbar: {
      show: false
    }
  },
  plotOptions: {
    bar: {
      horizontal: false,
      columnWidth: '55%',
      borderRadius: 4,
    },
  },
  colors: ['#60A5FA', '#8B5CF6'],
  dataLabels: {
    enabled: false
  },
  grid: {
    borderColor: '#E5E7EB',
    strokeDashArray: 3,
    xaxis: {
      lines: {
        show: false
      }
    }
  },
  xaxis: {
    categories: ['Jan', 'Feb', 'Mar', 'Apr', 'May', 'Jun', 'Jul', 'Aug', 'Sep', 'Oct', 'Nov', 'Dec'],
    labels: {
      style: {
        colors: '#6B7280',
        fontSize: '12px'
      }
    },
    axisBorder: {
      show: false
    },
    axisTicks: {
      show: false
    }
  },
  yaxis: {
    labels: {
      formatter: (value) => `$${value.toLocaleString()}`,
      style: {
        colors: '#6B7280',
        fontSize: '12px'
      }
    }
  },
  tooltip: {
    y: {
      formatter: (value) => `$${value.toLocaleString()}`
    }
  },
  legend: {
    position: 'top',
    horizontalAlign: 'left'
  }
})
</script>