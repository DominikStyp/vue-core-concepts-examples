<template>
  <button v-on:click.right="clickRight">Click Right Button</button>
  <button v-on:click.left="clickLeft('Hello from: ', $event)">
    Click Left Button
  </button>
</template>

<script>
export default {
  name: "EventModifiers",
  props: {
    myProp: String,
  },
  data() {
    return {};
  },
  methods: {
    clickRight() {
      alert("Clicked right button!");
    },
    clickLeft(param1, event) {
      alert("Clicked left button! " + param1 + event.target);
    },
  },
};
</script>

<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>