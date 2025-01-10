<script setup lang="ts">
import AttendanceOverview from '~/components/AttendanceOverview.vue';
import EmployeeList from '~/components/EmployeeList.vue';
import EmployeePerformance from '~/components/EmployeePerformance.vue';
import IncomeStatistics from '~/components/IncomeStatistics.vue';
import TodayUsedDevices from '~/components/TodayUsedDevices.vue';
import TotalEmployees from '~/components/TotalEmployees.vue';

</script>



<template>
   <div class="content flex-1 p-4">
    <div class="header flex flex-col md:flex-row md:items-center md:justify-between mb-4">
      <div>
        <h1 class="text-2xl font-bold">Good Morning, Sai</h1>
        <p class="text-gray-600">Welcome back!</p>
      </div>
      <div class="search-bar mt-4 md:mt-0">
        <input 
          type="text" 
          placeholder="Search..." 
          class="w-full md:w-64 px-4 py-2 border rounded-lg focus:outline-none focus:ring-2 focus:ring-purple-600"
        />
      </div>
    </div>
    <section class="widgets grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
      <TotalEmployees />
      <AttendanceOverview />
      <TodayUsedDevices />
    </section>
    <section class="grid grid-cols-1 md:grid-cols-2 gap-4 mt-4">
      <EmployeePerformance />
      <IncomeStatistics />
    </section>
    <EmployeeList class="mt-4" />
  </div>
    </template>