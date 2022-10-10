<template>
  <ComponentC />
  <h2>username from mainApp {{ name }}</h2>
</template>

<script>
import ComponentC from "./ComponentC.vue";
export default {
  name: "MainApp",
  components: {
    ComponentC,
  },
  data() {
    return {
      name: "birendra",
    };
  },
  provide() {
    return {
      username: this.name,
    };
  },
};
</script>

<style scoped></style>
