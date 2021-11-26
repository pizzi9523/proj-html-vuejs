<template>
  <section class="high_performance">
    <SectionTitle title="HIGH PERFORMANCE FACILITIES" />
    <div class="container">
      <div class="row">
        <div class="col-3" v-for="n in 6" :key="n">
          <div class="home_image_wrapper">
            <img :src="require(`../assets/images/home-image${n}.jpg`)" alt="" />
            <!-- <img src="../assets/images/home-image1.jpg" alt="" /> -->
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";

export default {
  data() {
    return {};
  },
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.high_performance {
  background-color: $secondary-bg-color;
  padding-bottom: 200px;
  .home_image_wrapper {
    opacity: 1;
    transform: scale(1);
    transition: transform 0.35s;
    padding: 10px;
    text-align: center;
    &:hover {
      transform: scale(1.03);
      cursor: pointer;
      img {
        box-shadow: 0px 0px 25px black;
      }
    }
    img {
      width: 100%;
      transition: all 0.35s;
    }
  }
}
</style>