<template>
  <div class="app">
    <myTest></myTest>
  </div>
</template>
<script>
import myTest from "./components/v-model和.sync";
export default {
  components: {
    myTest,
  },
  data() {
    return {};
  },
};
</script>
<style scoped>
.app {
  width: 900px;
}
</style>
