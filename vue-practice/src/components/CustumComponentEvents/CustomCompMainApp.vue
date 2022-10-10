<template>
  <div>
    <button @click="showPopup = true">Show Popup</button>
    <!-- <Popup v-show="showPopup" @close="showPopup = false" /> -->
    <Popup v-show="showPopup" @close="closePopup" />
  </div>
</template>

<script>
import Popup from "./Popup.vue";
export default {
  name: "CustomCompMainApp",
  components: {
    Popup,
  },
  data() {
    return {
      showPopup: false,
    };
  },
  methods: {
    closePopup(name) {
      this.showPopup = false;
      console.log("name", name);
    },
  },
};
</script>

<style scoped></style>
