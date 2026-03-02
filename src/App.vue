<script setup>
const route = useRoute()
const activePath = computed(() => route.path)
</script>

<template>
  <el-container class="app-layout">
    <el-header class="app-header">
      <div class="brand">Vite Vue Demo</div>
      <el-menu
        :default-active="activePath"
        mode="horizontal"
        router
        class="app-menu"
      >
        <el-menu-item index="/">首页</el-menu-item>
        <el-menu-item index="/about">关于</el-menu-item>
      </el-menu>
    </el-header>
    <el-main class="app-main">
      <router-view />
    </el-main>
  </el-container>
</template>

<style scoped>
.app-layout {
  min-height: 100vh;
}

.app-header {
  display: flex;
  align-items: center;
  gap: 24px;
  border-bottom: 1px solid #e5e7eb;
}

.brand {
  font-size: 18px;
  font-weight: 700;
  white-space: nowrap;
}

.app-menu {
  flex: 1;
  min-width: 0;
}

.app-main {
  background: #f7f8fa;
}
</style>
