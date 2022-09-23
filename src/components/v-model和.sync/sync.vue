<template>
  <div></div>
  <!-- 
    .sync作用
      实现父子组件数据之间的双向绑定，与v-model类似 
    .sync修饰符的原理
      <com1 :a.sync="num"></com1> 
      等价于
      <com1 :a="num" @update:a="val=>num=val"></com1> 

      相当于多了一个事件监听，事件名是update:a，回调函数中，会把接收到的值赋值给属性绑定的数据项中。

    -->
  <!-- 总结：
    sync与v-model区别是
      相同点：都是语法糖，都可以实现父子组件中的数据的双向通信。
      区别点：一个组件上只能有一个v-model，.sync修饰符可以有多个 -->
</template>

<script>
export default {
  name: "VuePractiseSync",

  data() {
    return {};
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped></style>
