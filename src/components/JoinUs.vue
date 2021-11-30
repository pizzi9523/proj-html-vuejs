<template>
  <section class="join_us">
    <div class="container">
      <div class="row join">
        <div class="content">
          <h2>Achieve Your Fitness Goals</h2>
          <p>
            Flexible membership packages to suit all levels of athlete and
            achive your fitness goals
          </p>
        </div>
        <button class="button_light">JOIN US</button>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.join_us {
  background-image: url("../assets/images/home-parallax.jpg");
  filter: hue-rotate($image-hue-rotate);
  background-position-y: -216px;
  padding: 60px;
  .join {
    justify-content: space-between;
    align-items: center;
    h2 {
      font-size: 32px;
      font-weight: 700;
      margin-bottom: 13px;
    }
    button {
      margin-right: 175px;
      color: $secondary-text-color;
      border-color: $secondary-text-color;
      transition: 0.5s;
      &:hover {
        transform: scale(1.1);
        color: $primary-text-color;
        border-color: $primary-text-color;
      }
    }
  }
}
</style>