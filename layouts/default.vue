<template>
  <div class="layout">
    <SidebarMenu />
    <main>
      <nuxt-page />
    </main>
  </div>
</template>

<style scoped>
.layout {
  display: flex;
}
main {
  flex: 1;
  padding: 20px;
}
</style>
