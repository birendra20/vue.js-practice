<template>
  <div>
    <h2>fullName -{{ firstName }} {{ lastName }}</h2>
    <h2>computed fullName- {{ fullName }}</h2>
    <!-- <h2>
      total-{{ items.reduce((total, curr) => (total = total + curr.price), 0) }}
    </h2> -->
    <button @click="items.push({ id: 4, title: 'keyboard', price: 45 })">
      add item
    </button>
    <h2>computed total - {{ total }}</h2>
  </div>
</template>

<script>
export default {
  name: "ComputedProperties",
  data() {
    return {
      firstName: "bruce",
      lastName: "wayne",
      items: [
        {
          id: 1,
          title: "tv",
          price: 100,
        },
        {
          id: 2,
          title: "phone",
          price: 200,
        },
        {
          id: 3,
          title: "laptop",
          price: 300,
        },
      ],
    };
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`;
    },
    total() {
      return this.items.reduce(
        (total, curr) => (total = total + curr.price),
        0
      );
    },
  },
};
</script>

<style scoped></style>
