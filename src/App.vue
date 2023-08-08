<template>
  <div class="top">
    <h1>KoderHq</h1>
  </div>

  <p>{{ greeting('Didy') }}</p>
</template>

<script>
export default {
  data() {
    return {
      name: "Didy",
    };
  },
  methods: {
    greeting: (name) => {
      return "Hello " + name;
    },
  },
};
</script>

<style>
.top {
  display: flex;
  width: 100%;
  color: cadetblue;
  justify-content: center;
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
