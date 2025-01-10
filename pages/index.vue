<script setup lang="ts">
import AttendanceOverview from '~/components/AttendanceOverview.vue';
import DashboardHeader from '~/components/DashboardHeader.vue';
import EmployeeList from '~/components/EmployeeList.vue';
import TodayUsedDevices from '~/components/TodayUsedDevices.vue';

</script>

<template>
<DashboardHeader />
<TotalEmployees />

      <EmployeePerformance />
      <IncomeStatistics />
<AttendanceOverview/>
<TodayUsedDevices/>
<EmployeeList />

</template>
  
