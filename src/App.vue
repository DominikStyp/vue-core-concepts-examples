<template>
  <emit-events @click-me="handleEmitted" />
</template>

<script>
import EmitEvents from "./components/EmitEvents.vue";

export default {
  name: "App",
  components: {
    EmitEvents: EmitEvents,
  },
  methods: {
    handleEmitted(event) {
      alert(event.target);
    },
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
</style>
