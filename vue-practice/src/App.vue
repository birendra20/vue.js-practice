<template>
  <Greet />
  <ConditinalRendering />
  <ListRendering />
  <ListAndKey />

  <!-- <Misc /> -->
</template>

<script>
import Greet from "./components/Greet.vue";
import ConditinalRendering from "./components/ConditionalRendering.vue";
import ListRendering from "./components/ListRendering.vue";
import ListAndKey from "./components/ListAndKey.vue";

// import Misc from "./components/Misc.vue";
export default {
  name: "App",
  components: {
    Greet,
    ConditinalRendering,
    ListRendering,
    ListAndKey,
    // Misc,
  },
  data() {
    return {};
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
