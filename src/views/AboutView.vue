<template>
  <div class="page">
    <el-card>
      <template #header>
        <span>About</span>
      </template>
      <p>这个页面用于演示 Vue Router 的多页面切换。</p>
      <el-tag type="success">当前路由: /about</el-tag>
    </el-card>
  </div>
</template>

<style scoped>
.page {
  padding: 20px;
}
</style>
