<template>
  <h2 v-for="name in names" :key="name">{{ name }}</h2>
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
</template>

<script>
export default {
  name: "ListRendering",
  data() {
    return {
      names: ["ramesh", "ambesh", "rajan"],
      fullNames: [
        { first: "bruce", last: "wayne" },
        { first: "birendra", last: "gupta" },
        { first: "ramesh", last: "iramala" },
      ],
    };
  },
};
</script>

<style scoped></style>
