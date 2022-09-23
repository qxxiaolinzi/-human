<template>
  <div>
    <h1>v-model指令</h1>
    <!-- <input type="text" v-model="username" /> -->
    <!-- <input
      type="text"
      :value="username"
      @input="(e) => (username = e.target.value)"
    /> -->

    <!-- 
      v-model的作用： 在表单元素或自定义组件上创建双向数据绑定
      v-model的本质就是一个语法糖， 比如说 在 input 和 textarea 元素上 会解析成 value属性和input事件；
      v-model 可以通过 model字段 来修改 v-model 绑定的属性和事件的名称
      model: {prop: 'value',event: 'input'}

      v-model 在组件上的使用
    -->

    <h1>{{ count }}</h1>
    <addsub v-model="count"></addsub>

  </div>
</template>

<script>
import addsub from './addsub.vue';
export default {
  components: { addsub },
  name: "VuePractiseIndex",

  data() {
    return {
      username: 11,
      count: 0,
    };
  },

  mounted() {},

  methods: {},
};
</script>
