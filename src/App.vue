<template>
  <div class="top">
    <h1>Full Name: {{ fullName }}</h1>
    <label class="margin">First Name: {{ firstName }}</label>
    <input class="margin input" type="text" v-model="firstName" />
    <label class="margin">Last Name: {{ lastName }}</label>
    <input class="margin input" type="text" v-model="lastName" />
  </div>
  <p>{{ num }}</p>
  <button @click="changeFullName">Change Name</button>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
    };
  },
  methods: {
    changeFullName() {
      this.fullName = "Chris Pratt";
    },
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
