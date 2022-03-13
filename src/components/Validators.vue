<template>
  <table>
    <tr>
      <th>E-mail</th>
      <th>Name</th>
      <th>Country</th>
    </tr>
    <tr>
      <td>{{ email }}</td>
      <td>{{ name }}</td>
      <td>{{ country }}</td>
    </tr>
  </table>
</template>

<script>
export default {
  props: {
    email: {
      type: String,
      required: true,
      validator: function (v) {
        return v.match(/[\w\d.-]+@[\w\d.-]+/gi);
      },
    },
    name: {
      type: String,
      required: true,
      validator: function (v) {
        return v.match(/[\w\d.-]+/gi);
      },
    },
    country: {
      type: String,
      required: true,
      validator: function (v) {
        return v.match(/[A-Z]{2,3}/gi);
      },
    },
  },
};
</script>