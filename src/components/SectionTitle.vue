<template>
  <div class="world_class">
    <h2>{{ title }}</h2>
    <img src="../assets/images/divider-xx-red.png" alt="" />
    <p v-if="text">
      {{ text }}
    </p>
  </div>
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

.world_class {
  text-align: center;

  background-color: $secondary-bg-color;
  padding: 80px;
  h2 {
    padding: 30px;
    font-size: 32px;
  }
  p {
    width: 750px;
    margin: auto;
    padding: 30px;
    color: $secondary-text-color;
  }
}
</style>