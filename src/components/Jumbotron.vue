<template>
  <section class="jumbotron">
    <div class="jumbo_text">
      <h1>NO PAIN NO GAIN</h1>
      <p>Motivation is what gets you started. Habit is what keeps you going.</p>
      <button>JOIN US TODAY</button>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.jumbotron {
  background-image: url("../assets/images/home-banner.jpg");
  background-size: cover;
  background-position-y: -20px;
  background-position-x: center;
  color: $primary-text-color;
  margin-top: -180px;
  min-height: 1000px;
  display: flex;
  text-align: center;
  justify-content: center;
  align-items: center;
  .jumbo_text {
    margin-top: 15px;
    h1 {
      font-size: 90px;
      padding: 10px;
    }

    p {
      font-size: 23px;
    }

    button {
      margin-top: 30px;
      padding: 13px 30px;
      background-color: transparent;
      color: $secondary-text-color;
      font-size: 16px;
      border: 1px solid $secondary-text-color;
      &:hover {
        cursor: pointer;
      }
    }
  }
}
</style>