<template>
  <aside class="w-64 bg-gray-100 h-screen p-6">
    <div class="flex items-center mb-8">
      <img src="/spectro.png" alt="Logo" class="w-10 h-10 mr-3" />
      <h1 class="text-lg font-semibold">TurHR</h1>
    </div>
    <nav>
      <ul class="space-y-4">
        <li><nuxt-link to="/" class="block text-gray-700 font-medium hover:text-purple-500">Dashboard</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Projects</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Calendar</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Leave Management</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Settings</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Notification</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Help & Center</nuxt-link></li>
      </ul>
    </nav>

    <div class="mt-8">
      <h2 class="text-sm font-semibold text-gray-600 uppercase">Team Management</h2>
      <ul class="space-y-4 mt-4">
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Performance</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Payrolls</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Invoices</nuxt-link></li>
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Employees</nuxt-link></li>
        <li>
          <nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Recruitment & Hiring</nuxt-link>
        </li>
      </ul>
    </div>

    <div class="mt-8">
      <h2 class="text-sm font-semibold text-gray-600 uppercase">Lists</h2>
      <ul class="space-y-4 mt-4">
        <li><nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Salary Information</nuxt-link></li>
        <li>
          <nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Compensation Breakdown</nuxt-link>
        </li>
        <li>
          <nuxt-link class="block text-gray-700 font-medium hover:text-purple-500">Project-specific Data</nuxt-link>
        </li>
      </ul>
    </div>

    <div class="mt-8">
      <h2 class="text-sm font-semibold text-gray-600 uppercase">Announcements</h2>
      <div class="mt-4 bg-white p-4 rounded shadow">
        <p class="text-gray-700">Stay updated with TurHR</p>
        <nuxt-link class="text-purple-500 font-medium hover:underline">Create Now</nuxt-link>
      </div>
    </div>
  </aside>
</template>
