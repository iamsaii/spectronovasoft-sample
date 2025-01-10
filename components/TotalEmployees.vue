<template>
    <div class="bg-white p-6 rounded-lg shadow-sm">
      <div class="flex justify-between items-center mb-6">
        <h3 class="font-medium text-gray-900">Total Employees</h3>
        <button class="text-gray-400 hover:text-gray-600">
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 5v.01M12 12v.01M12 19v.01M12 6a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2zm0 7a1 1 0 110-2 1 1 0 010 2z" />
          </svg>
        </button>
      </div>
  
      <div class="space-y-4">
        <!-- Fulltime Employees -->
        <div class="flex justify-between items-center">
          <div class="flex items-center space-x-2">
            <span class="text-2xl font-semibold">150</span>
            <span class="text-green-500 text-sm">+50</span>
          </div>
          <span class="text-gray-500 text-sm">Fulltime Employee</span>
        </div>
  
        <!-- Freelance Employees -->
        <div class="flex justify-between items-center">
          <div class="flex items-center space-x-2">
            <span class="text-2xl font-semibold">50</span>
            <span class="text-orange-500 text-sm">+10</span>
          </div>
          <span class="text-gray-500 text-sm">Freelance Employee</span>
        </div>
      </div>
    </div>
  </template>
  
