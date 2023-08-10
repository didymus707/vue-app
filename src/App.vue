<template>
  <div class="top">
    <p>Counter: {{ count }}</p>

    <button @click="count++">Increment</button>
    <button @click="count--">Decrement</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  computed: {
    fullName: {
      get() {
        return this.firstName + " " + this.lastName;
      },
      set(value) {
        const names = value.split(" ");
        this.firstName = names[0];
        this.lastName = names[1];
      },
    },
  },
  watch: {
    count(newValue, oldValue) {
      if (newValue > oldValue && newValue === 5)
        alert("Increasing the volume past 5 may damage your hearing");
    },
  },
};
</script>

<style scoped>
.top {
  width: 40%;
  display: flex;
  flex-direction: column;
  color: forestgreen;
}
.margin {
  margin-top: 8px;
}
.input {
  width: 28%;
  padding: 6px 12px;
  border-radius: 4px;
  border: 1px solid forestgreen;
}
</style>
