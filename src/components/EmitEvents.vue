<template>
  <button @click="handle">Click me!</button>
</template>
<script>
export default {
  // simplest version of emits
  // emits: ['click-me'],
  emits: {
    // this is not mandatory to add
    "click-me": function (event) {
      // here we can apply a validation rules
      // for the emitted values for the specified event
      return event.target instanceof HTMLButtonElement ? true : false;
    },
  },
  methods: {
    handle(event) {
      this.$emit("click-me", event);
    },
  },
};
</script>