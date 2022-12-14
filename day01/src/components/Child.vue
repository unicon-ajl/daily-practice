<template>
  <div class="child">
    <h1>我是Child组件（子组件）</h1>
  </div>
</template>

<script>
export default {
  name: "Child",
  components: {
  },
  setup() {
  }
};
</script>

<style>
.child{
  background: orange;
  padding: 10px;
}
</style>