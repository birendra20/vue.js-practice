<template>
  <div>
    <h2>this is a popup</h2>
    <button @click="$emit('close', 'birendra')">close Popup</button>
  </div>
</template>

<script>
export default {
  name: "Popup",
  emits: ["close"],
};
</script>

<style scoped></style>
