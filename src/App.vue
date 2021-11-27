<template>
  <div id="app">
    <SiteHeader :navMenu="navMenuOptions" />
    <SiteMain :blog="blog_post" />
    <SiteFooter
      :info="gym_info"
      :openingTimes="gym_openingTimes"
      :copyrightText="copyright"
      :blog="blog_post"
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

      blog_post: [
        {
          title: "Train with free weights or your body weight?",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img: "blog1",

          title_1: "To be number one, train like you're number two",
          content_1:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img_1: "blog4-400x289",
        },

        {
          title: "Nutritional advice thet will keep you training",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img: "blog6-400x400",

          title_1: "Top 5 mistakes every gym member makes",
          content_1:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img_1: "trainer2-600x445",
        },

        {
          title: "Simple principles for your next workout",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img: "trainer3",

          title_1: "The myths of shedding body fat explored",
          content_1:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img_1: "trainer1",
        },
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
