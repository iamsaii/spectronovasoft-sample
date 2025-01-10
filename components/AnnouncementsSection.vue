<template>
    <div class="bg-white p-6 rounded-lg shadow">
      <h3 class="text-lg font-semibold mb-4">Announcements</h3>
      <div class="space-y-4">
        <div>
          <h4 class="font-medium">Stay updated with TurHR</h4>
          <p class="text-gray-600 text-sm">Create New</p>
          <div class="flex mt-3">
            <!-- <img
              v-for="avatar in avatars"
              :key="avatar"
              :src="avatar"
              alt="Avatar"
              class="w-8 h-8 rounded-full border-2 border-white -ml-2"
            /> -->
            <div class="w-8 h-8 rounded-full bg-purple-500 text-white flex items-center justify-center -ml-2">
              +10
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const avatars = [
    '',
    '',
    '',
  ]
  </script>
  
 