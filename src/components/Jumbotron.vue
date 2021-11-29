<template>
  <section class="jumbotron">
    <div class="jumbo_text">
      <h1>NO PAIN NO GAIN</h1>
      <p>Motivation is what gets you started. Habit is what keeps you going.</p>
      <button class="button_light">JOIN US TODAY</button>
    </div>
    <!-- /.jumbo_text  -->
  </section>
  <!-- /.jumbotron  -->
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.jumbotron {
  background-image: url("../assets/images/home-banner.jpg");
  background-size: cover;
  background-position-y: -75px;
  background-position-x: center;
  color: $primary-text-color;
  margin-top: -180px;
  min-height: 1000px;
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
  .jumbo_text {
    margin-top: 135px;
    h1 {
      font-size: 125px;
      padding: 10px;
    }

    p {
      font-size: 23px;
    }

    button.button_light {
      margin-top: 30px;
    }
  }
}
</style>