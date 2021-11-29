<template>
  <div class="section_title">
    <h2>{{ title }}</h2>
    <img src="../assets/images/divider-xx-red.png" alt="" />
    <p v-if="text">
      {{ text }}
    </p>
  </div>
  <!-- /.section_title  -->
</template>

<script>
export default {
  props: {
    title: String,
    text: String,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.section_title {
  text-align: center;
  img {
    filter: hue-rotate($image-hue-rotate);
  }

  padding: 80px;
  h2 {
    padding: 30px;
    font-size: 32px;
  }
  p {
    width: 900px;
    margin: auto;
    padding: 30px;
    color: $secondary-text-color;
    line-height: 30px;
  }
}
</style>