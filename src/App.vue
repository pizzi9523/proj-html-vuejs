<template>
  <div id="app">
    <SiteHeader :navMenu="navMenuOptions" />
    <SiteMain />
    <SiteFooter
      :info="gym_info"
      :openingTimes="gym_openingTimes"
      :copyrightText="copyright"
    />
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

      gym_info: [
        {
          address: "12345 North Main Street, New York NY 555555",
          phone: "1.800.555.6789",
          email: "info@your-domain.com",
        },
      ],

      gym_openingTimes: [
        {
          weekday: "Monday - Friday",
          timeTable: "9:00 - 19:00",
        },
        {
          weekday: "Saturday - Sunday",
          timeTable: "9:00 - 21:00",
        },
      ],

      copyright: [
        "© Copyright 2015",
        "Avada Theme by ThemeFusion",
        "All Rights Reserved",
        "Powered by WordPress",
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
@import "./assets/scss/variables.scss";
@import "./assets/scss/common.scss";
</style>
