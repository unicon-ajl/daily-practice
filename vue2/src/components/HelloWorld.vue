<template>
  <div class="hello">
    <h2>我是HelloWorld组件</h2>
    <h3>父组件传递进来的数据：{{id}} - {{msg}}</h3>
    <!-- <h3>父组件传递进来的数据：{{$attrs.id}} - {{$attrs.msg}}</h3> -->

    <!-- 
      父组件传递内容给子组件，如果子组件内部没有定义插槽，则传递的内容作为虚拟节点保存在VueComponent的 $slots 属性上
      如果定义了插槽，那么虚拟节点会转换为真实节点，在界面中展示。
     -->
     <slot name="before"></slot>
     <slot></slot>
     <slot name="after"></slot>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  // 推荐使用props接收父组件传递进来的数据
  props: ['id', 'msg'], //接收而来的数据都绑定到VueComponent身上
  /* 
    父组件传递给子组件的数据，如果子组件通过props声明接收，那么数据会绑定到VueComponent身上；
    如果子组件没有声明接收，则会保存在VueComponent的 $attrs 属性上
  */
  mounted() {
    console.log(this) //组件的实例对象
  }
}
</script>

<style scoped>
.hello{
  background: orange;
  padding: 10px;
}
</style>
