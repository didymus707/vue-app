<template>
  <div class="top">
    <h1>Full Name: {{ firstName }} {{ lastName }}</h1>
    <label class="margin">First Name: {{ firstName }}</label>
    <input class="margin input" type="text" v-model="firstName" />
    <label class="margin">Last Name: {{ lastName }}</label>
    <input class="margin input" type="text" v-model="lastName" />
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
    };
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
