<template>
  <div id="app">
    <SiteHeader :navMenu="navMenuOptions" />
    <SiteMain />
    <SiteFooter />
  </div>
</template>

<script>
import SiteHeader from "./components/SiteHeader.vue";
import SiteMain from "./components/SiteMain.vue";
import SiteFooter from "./components/SiteFooter.vue";

export default {
  name: "App",
  data() {
    return {
      navMenuOptions: [
        "Home",
        "About Us",
        "Facilities",
        "Membership",
        "Testimonials",
        "Blog",
      ],
    };
  },
  components: {
    SiteHeader,
    SiteMain,
    SiteFooter,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/common.scss";
</style>
