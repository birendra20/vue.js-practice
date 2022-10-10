<template>
  <hr />
  <div>{{ name }}</div>
  <div>
    <button v-on:click="name = 'batman'">Change name</button>
    <button v-on:mouseover="name = 'batman'">Change name</button>
  </div>
  <h1>{{ count }}</h1>
  <button v-on:click="count += 1">increment</button>
  <button v-on:click="count -= 1">decrement</button>
  <div>
    <button v-on:click="increment">increment</button>
    <button v-on:click="decrement">decrement</button>
  </div>
  <div>
    <button v-on:click="increment5(5)">increment5</button>
    <button v-on:click="decrement5(5)">decrement5</button>
  </div>
  <hr />
</template>

<script>
export default {
  name: "EventHandling",
  data() {
    return {
      name: "birendra",
      count: 0,
    };
  },
  methods: {
    increment() {
      this.count += 1;
    },
    decrement() {
      this.count -= 1;
    },
    increment5(num) {
      this.count += num;
    },
    decrement5(num) {
      this.count -= num;
    },
  },
};
</script>

<style scoped></style>
