<script setup lang="ts">
const count = ref(0)
const isLoading = ref(false)
function onRefresh() {
  setTimeout(() => {
    showToast('刷新成功')
    setTimeout(() => {
      isLoading.value = false
    }, 400)
    count.value++
  }, 1000)
}
</script>

<template>
  <div class="h-100vh w-100vw bg-#f7f7f7">
    <div class="h-30vh w-100vw bg-pink" />
    <PullRefresh v-model="isLoading" @refresh="onRefresh">
      <template #content>
        <div class="h-30vh w-100vw">
          <p>刷新次数: {{ count }}</p>
        </div>
      </template>
    </PullRefresh>
  </div>
</template>

<style lang="less" scoped>
</style>

<route lang="json">
{
  "name": "home",
  "meta": {
    "title": "主页",
    "i18n": "menus.home"
  }
}
</route>
