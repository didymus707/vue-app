<script>
import HelloWorld from './components/HelloWorld';
import ChildGreeting from "./components/ChildGreeting";
import GreetingMessage from "./components/GreetingMessage";
export default {
  components: {
    GreetingMessage,
    ChildGreeting,
    HelloWorld,
  },
  computed: {
    filter() {
      return this.users.filter((user) => user.age >= 18);
    },
  },
  provide: {
    firstName: 'Scott',
    lastName: 'Lang'
  }
};
</script>

<template>
  <greeting-message />
  <hello-world firstName="Scott" lastName="Lang" />
  <child-greeting firstName="Peter" lastName="Parker" />
  <child-greeting firstName="Tony" lastName="Stark" />
  <child-greeting firstName="Thor" lastName="Son of Odin" />
</template>
