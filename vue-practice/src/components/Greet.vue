<template>
  <div>hello {{ name }} a.k.a {{ heroName }}</div>
</template>

<script>
export default {
  name: "Greet",
  props: ["name", "heroName"],
};
</script>

<style scoped></style>
