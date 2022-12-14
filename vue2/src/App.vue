<template>
  <div id="app">
    <h1>Vue2.x演示组件通信和插槽</h1>
    <!-- 使用组件 -->
    <!-- 组件通信：步骤一：父组件向子组件传递数据 -->
    <HelloWorld id="1001" msg="你好啊！">
      <template v-slot:before>
        <h3>我是前置插槽</h3>
      </template>
      <span>我是默认插槽</span>
      <template v-slot:after>
        <h3>我是后置插槽</h3>
      </template>
    </HelloWorld>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app{
  background: gray;
  padding: 10px;
}
</style>


