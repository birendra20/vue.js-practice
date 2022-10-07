<template>
  <div>{{ greet }} {{ name }} binding data</div>
  <div v-text="channels"></div>
  <div v-html="channel"></div>
  <div v-html="hack"></div>
  <h2 v-bind:id="headingId">Heading(Binding to Attributes )</h2>

  <button v-bind:disabled="isDisabled">Binding to Attributes</button>
  <h2 class="underline">Binding styles(static class eg)</h2>
  <h2 v-bind:class="status">Binding styles(dynamic class eg)</h2>
  <h2 v-bind:class="isPromoted && 'promoted'">
    Binding styles(dynamic class eg)
  </h2>
  <h2 v-bind:class="isSoldout ? 'sold-out' : 'new'">
    conditionally Binding styles(dynamic class eg)
  </h2>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      greet: "hello",
      name: "birendra",
      channels: "binding text",
      channel: "<b>Binding Html</b>",
      hack: `<a href="#" onclick="alert('you have been hacked!')">win a prize!</a>`,
      headingId: "heading",
      isDisabled: false,
      status: "danger",
      isPromoted: true,
      isSoldout: false,
    };
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
.underline {
  text-decoration: underline;
}
.promoted {
  font-style: italic;
}
.new {
  color: aqua;
}
.sold-out {
  color: red;
}
</style>
