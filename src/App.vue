<template>
  <div class="top">
    <p>Your name: {{ name }}</p>
    <input type="text" @input="getInput($event, 'Johnson')" />
    <!-- lock this counter after first render -->
    <p v-once>Initial value: {{ counter }}</p>
    <p>Updated value: {{ counter }}</p>

    <button @click="increment">Increment</button>
    <button @click="decrement">Decrement</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "",
      counter: 10,
    };
  },
  methods: {
    getInput(event, lastName) {
      this.name = event.target.value + " " + lastName;
    },
    increment() {
      this.counter++;
    },
    decrement() {
      this.counter--;
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
