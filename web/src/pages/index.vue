<script setup lang="ts">
const count = ref(0)
const isLoading = ref(false)
function onRefresh() {
  setTimeout(() => {
    showToast('刷新成功')
    // isLoading.value = false
    count.value++
  }, 1000)
}
</script>

<template>
  <div class="h-100vh w-100vw bg-#f7f7f7">
    <van-pull-refresh
      v-model="isLoading"
      :head-height="80"
      @refresh="onRefresh"
    >
      <!-- 下拉提示，通过 scale 实现一个缩放效果 -->
      <template #pulling="props">
        <!-- <img
          class="doge"
          src="https://fastly.jsdelivr.net/npm/@vant/assets/doge.png"
          :style="{ transform: `scale(${props.distance / 80})` }"
        > -->
        <div class="test flex items-center justify-center">
          <span class="icon" />
          <p>释放立即加载{{ props.distance }}</p>
        </div>
      </template>

      <!-- 释放提示 -->
      <template #loosing>
        <div class="test flex items-center justify-center">
          <span class="icon" />
          <p>释放提示</p>
        </div>
      </template>

      <!-- 加载提示 -->
      <template #loading>
        <div h-100 flex flex-col items-center justify-center>
          <span h-4rem w-4rem />
          <p h-4rem text-3rem lh-4rem>
            加载提示
          </p>
        </div>
      </template>
      <div class="h-100vh w-100vw">
        <p>刷新次数: {{ count }}</p>
      </div>
    </van-pull-refresh>
  </div>
</template>

<style lang="less" scoped>
.doge {
  width: 4rem;
  height: 100%;
  margin-top: 8px;
  border-radius: 4px;
}
.test {
  .icon {
    width: 2rem;
    height: 2rem;
  }
}
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
