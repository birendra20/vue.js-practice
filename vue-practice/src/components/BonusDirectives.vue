<template>
  <h2 v-once>{{ name }}</h2>
  <button @click="name = 'batman'">Change name</button>
</template>

<script>
export default {
  name: "BonusDirectives",
  data() {
    return {
      name: "birendra",
    };
  },
};
</script>

<style scoped></style>
