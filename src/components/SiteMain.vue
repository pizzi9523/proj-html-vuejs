<template>
  <main>
    <Jumbotron />
    <SignUp />
    <Services />
    <Result />
    <HighPerformance />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SignUp from "./SignUp.vue";
import Services from "./Services.vue";
import Result from "./Result.vue";
import HighPerformance from "./HighPerformance.vue";

export default {
  components: {
    Jumbotron,
    SignUp,
    Services,
    Result,
    HighPerformance,
  },
};
</script>


<style lang="scss">
</style>