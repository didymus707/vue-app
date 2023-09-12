<script>
export default { props: ["firstName", "lastName"] };
</script>

<template>
  <p>Hello {{ firstName }} {{ lastName }}</p>
</template>
