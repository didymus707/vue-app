<template>
  <div class="top">
    <h1>{{ name }} ({{ ego }})</h1>
    <button @click="changeName('Andrea'), changeEgo('engineer')">
      Click
    </button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "KoderHq",
      ego: "guy",
    };
  },
  methods: {
    changeName(name) {
      this.name = name;
    },
    changeEgo(ego) {
      this.ego = ego;
    },
  },
};
</script>

<style scoped>
.top {
  color: forestgreen;
}
</style>
>
