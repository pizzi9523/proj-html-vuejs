<template>
  <main>
    <Jumbotron />
    <SignUp />
    <Services />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SignUp from "./SignUp.vue";
import Services from "./Services.vue";

export default {
  components: {
    Jumbotron,
    SignUp,
    Services,
  },
};
</script>


<style lang="scss">
</style>