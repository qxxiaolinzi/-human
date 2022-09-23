<template>
  <div>
    <button @click="sub">-</button>
    {{ value }}
    <button @click="add">+</button>
  </div>
</template>

<script>
export default {
  name: "VuePractiseAddsub",
  model: {
    event: "change",
  },

  props: {
    value: {
      type: Number,
      default: 0,
    },
  },
  data() {
    return {};
  },

  mounted() {},

  methods: {
    add() {
      this.$emit("change", this.value + 1);
    },
    sub() {
      this.$emit("change", this.value - 1);
    },
  },
};
</script>

<style lang="scss" scoped></style>
