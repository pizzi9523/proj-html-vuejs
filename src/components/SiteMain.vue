<template>
  <main>
    <Jumbotron />
    <SignUp />
    <Services />
    <ResultReview />
    <HighPerformanceFacilities />
    <TestimonialBanner />
    <Trainers />
    <PerformanceNews :blog="blog" />
    <JoinUs />
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import SignUp from "./SignUp.vue";
import Services from "./Services.vue";
import ResultReview from "./ResultReview.vue";
import HighPerformanceFacilities from "./HighPerformanceFacilities.vue";
import TestimonialBanner from "./TestimonialBanner.vue";
import Trainers from "./Trainers.vue";
import PerformanceNews from "./PerformanceNews.vue";
import JoinUs from "./JoinUs.vue";

export default {
  components: {
    Jumbotron,
    SignUp,
    Services,
    ResultReview,
    HighPerformanceFacilities,
    TestimonialBanner,
    Trainers,
    PerformanceNews,
    JoinUs,
  },

  props: {
    blog: Array,
  },
};
</script>


<style lang="scss">
</style>