<template>
  <h2 v-if="num === 0">The number is Zero</h2>
  <h2 v-else-if="num < 0">The number is negative</h2>
  <h2 v-else-if="num > 0">The number is positive</h2>
  <h2 v-else>The number is not a number</h2>

  <template v-if="display">
    <h2>Hello</h2>
    <h2>welcome To</h2>
    <h2>Vue.js</h2>
  </template>
  <h2 v-show="showElement">using v-show</h2>
  <h2 v-if="showElement">using v-if</h2>
</template>

<script>
export default {
  name: "ConditinalRendering",
  data() {
    return {
      num: "",
      display: true,
      showElement: true,
    };
  },
};
</script>

<style scoped></style>
