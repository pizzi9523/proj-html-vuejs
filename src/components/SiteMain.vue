<template>
  <main>
    <Jumbotron />
    <SignUp />
    <Services />
    <Result />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SignUp from "./SignUp.vue";
import Services from "./Services.vue";
import Result from "./Result.vue";

export default {
  components: {
    Jumbotron,
    SignUp,
    Services,
    Result,
  },
};
</script>


<style lang="scss">
</style>