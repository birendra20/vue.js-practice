<template>
  <h2 v-for="name in names" :key="name">{{ name }}</h2>
  <hr />
  <h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
  <hr />
  <h2 v-for="name in fullNames" :key="name.first">
    {{ name.first }} {{ name.last }}
  </h2>
  <hr />
  <div v-for="actor in actors" :key="actor.name">
    <h1>{{ actor.name }}</h1>
    <h1>{{ actor.movies[0] }}</h1>
    <hr />
    <h3 v-for="movie in actor.movies" :key="movie">{{ movie }}</h3>
  </div>
  <hr />
  <h2 v-for="value in myInfo" :key="value">{{ value }}</h2>
  <hr />
  <h2 v-for="(value, key, index) in myInfo" :key="value">
    {{ index }} {{ key }} {{ value }}
  </h2>
  <hr />
  <hr />
  <template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr />
  </template>
  <hr />
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
      actors: [
        { name: "christian bale", movies: ["batman", "the Prestige"] },
        { name: "di caprio", movies: ["titanic", "inception"] },
      ],
      myInfo: {
        name: "vishwas",
        channel: "codeEvaluation",
        course: "Vue 3",
      },
    };
  },
};
</script>

<style scoped></style>
