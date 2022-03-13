<template>
  <ul>
    <li v-for="user in users" :key="user.id">
      {{ user.name }}: {{ user.email }}
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { id: 1, name: "Noob", email: "admin@examle.com" },
        { id: 2, name: "Neeb", email: "neeb@examle.com" },
        { id: 3, name: "Stats", email: "stats@examle.com" },
      ],
    };
  },
};
</script>