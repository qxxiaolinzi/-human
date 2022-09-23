<template>
  <div>
    <h1>v-for 和 v-if 为什么 不推荐一起使用</h1>
    <template>
      <h2 v-for="item in list1" :key="item">{{ item }}</h2>
    </template>

    <!-- 场景1： 只要求展示 大于等于5的数据 -->
    <!-- 场景2： 当showList 为true 的时候 才渲染列表 -->

    <!-- 
    1. 实践中不应该把v-for和v-if放一起 
    2.在vue2中，v-for的优先级是高于v-if，会先渲染整个列表，然后再去隐藏，相当于在做无用功，浪费性能
    3. 如何解决 ？ 
      1. 结合计算属性，把真正要展示的列表渲染出来。
      2. v-if 移动至容器元素上 (比如 ul、ol)或者外面包一层template。 -->
  </div>
</template>

<script>
export default {
  name: "VuePractiseIndex",

  data() {
    return {
      list: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    };
  },

  mounted() {},

  methods: {},
};
</script>

<style lang="scss" scoped></style>
