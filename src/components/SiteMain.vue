<template>
  <main>
    <Jumbotron />
    <SignUp />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SignUp from "./SignUp.vue";

export default {
  components: {
    Jumbotron,
    SignUp,
  },
};
</script>

<style lang="scss">
</style>