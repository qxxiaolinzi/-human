<template>
  <div>
    <h1>父子组件生命周期的执行顺序</h1>
    <child :count="count"></child>
    <button @click="count++">click {{ count }}</button>

    <!-- 
    1. 父子组件加载: 父beforecreate -> 父created -> 父beforeMount -> 子beforeCreate
    -> 子created -> 子beforeMount -> 子mounted -> 父mounted 
    
    2. 更新过程:
    父beforeUpdate->子beforeUpdate->子updated->父updated

    3. 销毁过程:
    父beforeDestroy->子beforeDestroy->子destroyed->父destroyed -->
  </div>
</template>

<script>
import child from "./child.vue";
export default {
  name: "VuePractiseParent",
  components: {
    child,
  },
  data() {
    return {
      count: 0,
    };
  },
  beforeCreate() {
    console.log("father - beforeCreate");
  },
  created() {
    console.log("father - created");
  },
  beforeMount() {
    console.log("father - beforeMount");
  },
  mounted() {
    console.log("father - mounted");
  },
  beforeUpdate() {
    console.log("father - beforeUpdate");
  },
  updated() {
    console.log("father - updated");
  },
  beforeDestroy() {
    console.log("father - beforeDestroy");
  },
  destroyed() {
    console.log("father - destroyed");
  },

  methods: {},
};
</script>

<style lang="scss" scoped></style>
