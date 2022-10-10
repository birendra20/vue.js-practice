<template>
  <div>{{ 12 * 365 }}</div>
  <h2>add method {{ add(10, 20, 30) }}</h2>
  <h2>add method {{ add(1, 20, 30) }}</h2>
  <h2>multiply method {{ multiply(20) }}</h2>
</template>

<script>
export default {
  name: "Methods",
  data() {
    return {
      baseMultiplier: 5,
    };
  },
  methods: {
    add(a, b, c) {
      return a + b + c;
    },
    multiply(num) {
      return num * this.baseMultiplier;
    }, //if we try a method as a arrow function we will get cannot read property of
  }, //"baseMultiplier" of undefined
};
</script>

<style lang="less" scoped></style>
