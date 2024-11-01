<script setup lang="ts">
// 定义 props，使用 TypeScript 进行类型注解
const props = withDefaults(defineProps<{
  modelValue: boolean
}>(), {
  modelValue: false,
})
// 定义 emits，使用 TypeScript 进行类型注解
const emit = defineEmits<{
  (e: 'update:modelValue', value: boolean): void
  (e: 'refresh'): void
}>()

// 响应式变量，用于 v-model 双向绑定
const isLoading = ref(props.modelValue)

// 监听 modelValue 的变化，同步更新 inputValue
watch(() => props.modelValue, (newValue) => {
  isLoading.value = newValue
})

watch(() => isLoading.value, () => {
  emit('update:modelValue', isLoading.value)
})

const pullHead = 60
function onRefresh() {
  emit('refresh')
}
</script>

<template>
  <van-pull-refresh
    v-model="isLoading"
    :head-height="pullHead"
    :disabled="isLoading"
    @refresh="onRefresh"
  >
    <!-- 下拉提示，通过 scale 实现一个缩放效果 -->
    <template #pulling>
      <div class="pullBox pullPull flex flex-col items-center">
        <div class="icon flex items-center justify-center">
          <van-icon name="arrow-down" size="1.2rem" />
        </div>
        <p>下拉即可刷新...</p>
      </div>
    </template>

    <!-- 释放提示 -->
    <template #loosing="props">
      <div class="pullBox pullLoos flex flex-col items-center">
        <!-- , top: `${-props.distance}px`  -->
        <div class="icon" :style="{ height: `${props.distance - pullHead || 0}px`, top: `${-(props.distance - pullHead) + 20}px`, opacity: `${props.distance < pullHead ? '0' : '1'}` }" />
        <p>释放提示</p>
      </div>
    </template>

    <!-- 加载提示 -->
    <template #loading>
      <div class="pullBox pullLoad flex flex-col items-center">
        <div class="icon flex items-center justify-center">
          <van-icon name="clock-o" size="1.2rem" />
        </div>
        <p h-4rem text-3rem lh-4rem>
          加载提示
        </p>
      </div>
    </template>
    <!-- 使用 v-slot 指令定义一个名为 "content" 的插槽，并传递额外的属性 :someProp="someValue" -->
    <slot name="content" />
  </van-pull-refresh>
</template>

<style lang="less" scoped>
:root {
  --van-pull-refresh-head-height: 60px;
}
:deep(.van-pull-refresh__head) {
  overflow: revert-layer !important;
  // background-color: lightblue;
}
.doge {
  width: 4rem;
  height: 100%;
  margin-top: 8px;
  border-radius: 4px;
}
.pullBox {
  position: relative;
  width: 100%;
  height: 100%;
  .icon {
    width: 1rem;
    height: auto;
    border-radius: 1rem;
    border: 1px solid #999;
  }
  p {
    width: 100%;
    height: 1.25rem;
    line-height: 1.25rem;
    position: absolute;
    bottom: 0.25rem;
    left: 0;
    text-align: center;
    // background: pink;
  }
}
.pullPull,
.pullLoad {
  .icon {
    margin-top: 0.75rem;
    width: 1.5rem;
    height: 1.5rem;
    border: none;
    border-radius: 0;
  }
}
.pullLoos {
  .icon {
    position: fixed;
    display: block;
    top: 4px;
    left: 50%;
    transform: translateX(-50%);
    font-size: 18px;
  }
}
</style>
