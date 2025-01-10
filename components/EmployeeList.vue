<template>
    <div class="bg-white p-6 rounded-lg shadow">
      <h3 class="text-lg font-semibold mb-4">All Employees</h3>
      <table class="min-w-full bg-white">
        <thead>
          <tr>
            <th class="py-2 px-4 border-b border-gray-200">Employee ID</th>
            <th class="py-2 px-4 border-b border-gray-200">Employee Name</th>
            <th class="py-2 px-4 border-b border-gray-200">Email</th>
            <th class="py-2 px-4 border-b border-gray-200">Role</th>
            <th class="py-2 px-4 border-b border-gray-200">Departments</th>
            <th class="py-2 px-4 border-b border-gray-200">Status</th>
            <th class="py-2 px-4 border-b border-gray-200">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="employee in employees" :key="employee.id" class="hover:bg-gray-100">
            <td class="py-2 px-4 border-b border-gray-200">{{ employee.id }}</td>
            <td class="py-2 px-4 border-b border-gray-200">{{ employee.name }}</td>
            <td class="py-2 px-4 border-b border-gray-200">{{ employee.email }}</td>
            <td class="py-2 px-4 border-b border-gray-200">{{ employee.role }}</td>
            <td class="py-2 px-4 border-b border-gray-200">{{ employee.department }}</td>
            <td class="py-2 px-4 border-b border-gray-200">
              <span :class="employee.status === 'Full-time' ? 'bg-green-100 text-green-800' : 'bg-yellow-100 text-yellow-800'"
                    class="px-2 py-1 rounded-full text-xs">
                {{ employee.status }}
              </span>
            </td>
            <td class="py-2 px-4 border-b border-gray-200">
              <button class="text-purple-500 hover:text-purple-700">Edit</button>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </template>
  
  <script setup>
  
  const employees = ref([
    { id: 'TUR871219', name: 'Ahsan Tapadar', email: 'ahsan.t@mall.com', role: 'Sr UI/UX Designer', department: 'Team Projects', status: 'Full-time' },
    { id: 'TUR85103', name: 'Washi Bin M.', email: 'washi.t@mall.com', role: 'Lead Product Designer', department: 'Head of Projects', status: 'Full-time' },
    { id: 'TUR751481', name: 'Kayes Ahmed', email: 'kayes.t@mall.com', role: 'Sr UX Designer', department: 'Client & Team Work', status: 'Full-time' },
    { id: 'TUR061481', name: 'Turja Sen Das', email: 'turja.t@mall.com', role: 'Mid UI Designer', department: 'Case Study', status: 'Freelance' },
  ])
  </script>
  
 