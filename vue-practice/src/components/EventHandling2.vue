<template>
  <div>{{ name }}</div>
  <div>
    <button @click="changeName($event), increment5(5, $event)">
      Change name
    </button>
    <button @click="name = 'batman'">Change name</button>
  </div>
  <h1>{{ count }}</h1>
  <button @click="count += 1">increment</button>
  <button @click="count -= 1">decrement</button>
  <div>
    <button @click="increment">increment</button>
    <button @click="decrement">decrement</button>
  </div>
  <div>
    <button @click="increment5(5, $event)">increment5</button>
    <button @click="decrement5(5)">decrement5</button>
  </div>
  <hr />
</template>

<script>
export default {
  name: "EventHandling2",
  data() {
    return {
      name: "birendra",
      count: 0,
    };
  },
  methods: {
    changeName(event) {
      this.name = "batman";
      console.log("event", event);
    },
    increment() {
      this.count += 1;
    },
    decrement() {
      this.count -= 1;
    },
    increment5(num, event) {
      this.count += num;
      console.log("event", event);
    },
    decrement5(num) {
      this.count -= num;
    },
  },
};
</script>

<style scoped></style>
