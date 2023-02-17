<template>
  <!-- <Greet name="bruce" heroName="batman" />
  <Greet name="diana" heroName="wonder women" />
  <Greet name="clark" heroName="superwomen" />
  <Greet :name="name" :heroName="channel" />
  <ConditinalRendering />
  <ListRendering />
  <ListAndKey />
  <ConditionalListRendering />
  <Methods />
  <EventHandling />

  <EventHandling2 />
  <FormHandling />
  <BonusDirectives />
  <ComputedProperties /> -->
  <Article title="Article Title" :likes="50" :isPublished="true" />

  <MainApp />
  <CustomCompMainApp />
  <!-- <Misc /> -->
</template>

<script>
// import Greet from "./components/Greet.vue";
// import ConditinalRendering from "./components/ConditionalRendering.vue";
// import ListRendering from "./components/ListRendering.vue";
// import ListAndKey from "./components/ListAndKey.vue";
// import ConditionalListRendering from "./components/ConditionalListRendering.vue";
// import Methods from "./components/Methods.vue";
// import EventHandling from "./components/EventHandling.vue";
// import EventHandling2 from "./components/EventHandling2.vue";
// import FormHandling from "./components/FormHandling.vue";
// import BonusDirectives from "./components/BonusDirectives.vue";
// import ComputedProperties from "./components/ComputedProperties.vue";
import Article from "./components/PropTypesAndValidation.vue";
import MainApp from "./components/ProvideAndInject/MainApp.vue";
import CustomCompMainApp from "./components/CustumComponentEvents/CustomCompMainApp.vue";

// import Misc from "./components/Misc.vue";
export default {
  name: "App",
  components: {
    // Greet,
    // ConditinalRendering,
    // ListRendering,
    // ListAndKey,
    // ConditionalListRendering,
    // Methods,
    // EventHandling,
    // EventHandling2,
    // FormHandling,
    // BonusDirectives,
    // ComputedProperties,
    Article,
    MainApp,
    CustomCompMainApp,
    // Misc,
  },
  data() {
    return {
      name: "birendra",
      channel: "biren",
    };
  },
};
console.log("Welcome");
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: #2c3e50;
  margin-top: 60px;
}
</style>
