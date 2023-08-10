<template>
  <template v-for="user in filter" :key="user.name">
    <p>{{ user.name }} is at the age where he can vote</p>
  </template>
</template>

<script>
export default {
  data() {
    return {
      users: [
        { name: "De", age: 33 },
        { name: "Andre", age: 34 },
        { name: "Yedlin", age: 29 },
        { name: "Stefan", age: 18 },
        { name: "Tanitoluwa", age: 7 },
        { name: "Toluwalase", age: 7 },
      ],
    };
  },
  computed: {
    filter() {
      return this.users.filter((user) => user.age >= 18);
    },
  },
};
</script>
