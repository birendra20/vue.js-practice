<template>
  <h2>ComponentF</h2>
  <h2>Component F username {{ username }}</h2>
</template>

<script>
export default {
  name: "ComponentF",
  inject: ["username"],
};
</script>

<style scoped></style>
