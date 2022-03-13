<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <Validators
    v-for="user in users"
    :key="user.id"
    :email="user.email"
    :name="user.name"
    :country="user.country"
  />
</template>

<script>
import usersMock from "./mockData/users.json";
import Validators from "./components/Validators.vue";

export default {
  data() {
    return {
      users: usersMock,
    };
  },
  components: {
    Validators: Validators,
  },
};
</script>
