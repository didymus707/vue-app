<script>
import GreetingMessage from "./components/GreetingMessage";
import ChildGreeting from "./components/ChildGreeting";
export default {
  components: {
    GreetingMessage,
    ChildGreeting,
  },
  computed: {
    filter() {
      return this.users.filter((user) => user.age >= 18);
    },
  },
};
</script>

<template>
  <greeting-message />
  <child-greeting firstName="Scott" lastName="Lang" />
  <child-greeting firstName="Peter" lastName="Parker" />
  <child-greeting firstName="Tony" lastName="Stark" />
  <child-greeting firstName="Thor" lastName="Son of Odin" />
</template>
