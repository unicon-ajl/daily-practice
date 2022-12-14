<template>
  <div class="app">
    <h1>我是App组件（祖先组件）</h1>
    <!-- 同步引入组件：如果该组件没有加载完毕，App组件也不会显示，App和Child是同时显示的 -->
    <!-- 异步引入组件：如果该组件没有加载完毕，App组件先显示，然后Child加载完毕再显示 -->
    <Suspense>
      <!-- 内容 -->
      <template v-slot:default>
        <Child></Child>
      </template>
      <!-- 提示 -->
      <template v-slot:fallback>
        <h3>稍等，内容加载中</h3>
      </template>
    </Suspense>
  </div>
</template>

<script>
// 同步引入组件（静态引入组件）
// import Child from "./components/Child";

// 异步引入组件
import { defineAsyncComponent } from "vue";
// 完整写法
// const Child = defineAsyncComponent(() => {
//   return import("./components/Child");
// });
// 简洁写法
const Child = defineAsyncComponent(()=>import('./components/Child'))

export default {
  name: "App",
  components: {
    Child,
  },
  setup() {},
};
</script>

<style>
.app {
  background: gray;
  padding: 10px;
}
</style>
