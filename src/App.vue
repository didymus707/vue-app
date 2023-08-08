<template>
  <p>Moustache syntax wraps the data property in double curly braces.</p>
  <p v-pre>Example: {{ name }}</p>

  <p>The resulting output will be the value of the data property.</p>
  <p>Example: {{ name }}</p>
</template>

<script>
export default {
  data() {
    return {
      name: 'John Doe'
    }
  }
}
</script>

<style>
.top {
  display: flex;
  width: 100%;
}
.btn {
  margin-left: 8px;
}
.valid {
  color: forestgreen;
}
.invalid {
  color: crimson;
}
.text-22 {
  font-size: 16px;
}
.bold {
  font-weight: bold;
}
.italic {
  font-style: italic;
}
</style>
