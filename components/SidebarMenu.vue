<template>
    <aside class="w-64 bg-gray-100 h-screen p-6">
      <div class="flex items-center mb-8">
        <!-- <img src="/path-to-logo.png" alt="Logo" class="w-10 h-10 mr-3" /> -->
        <h1 class="text-lg font-semibold">TurHR</h1>
      </div>
      <nav>
        <ul class="space-y-4">
          <li><nuxt-link to="/" class="block text-gray-700 font-medium hover:text-purple-500">Dashboard</nuxt-link></li>
          <li><nuxt-link to="/projects" class="block text-gray-700 font-medium hover:text-purple-500">Projects</nuxt-link></li>
          <li><nuxt-link to="/calendar" class="block text-gray-700 font-medium hover:text-purple-500">Calendar</nuxt-link></li>
          <li><nuxt-link to="/leave-management" class="block text-gray-700 font-medium hover:text-purple-500">Leave Management</nuxt-link></li>
          <li><nuxt-link to="/settings" class="block text-gray-700 font-medium hover:text-purple-500">Settings</nuxt-link></li>
          <li><nuxt-link to="/notifications" class="block text-gray-700 font-medium hover:text-purple-500">Notification</nuxt-link></li>
          <li><nuxt-link to="/help-center" class="block text-gray-700 font-medium hover:text-purple-500">Help & Center</nuxt-link></li>
        </ul>
      </nav>
    </aside>
  </template>
  
