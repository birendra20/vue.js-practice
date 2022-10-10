<template>
  <template v-for="name in names" :key="name">
    <h2 v-if="name === 'clark'">{{ name }}</h2>
  </template>
</template>

<script>
export default {
  name: "ConditionalListRendering",
  data() {
    return { names: ["bruce", "clark", "diana"] };
  },
};
</script>

<style scoped></style>
