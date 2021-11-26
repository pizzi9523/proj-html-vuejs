<template>
  <section class="testimonial">
    <div class="banner">
      <div class="banner_text">
        <p class="cit">
          "I fear not the man who has practiced 10,000 kicks once, but I fear
          the man who has practiced one kick 10,000 times"
        </p>

        <img src="../assets/images/divider-white-xx.png" alt="" />
        <p class="author_cit"><strong>BRUCE LEE • QUOTE OF THE DAY</strong></p>
      </div>
    </div>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss">
section.testimonial {
  background-image: url("../assets/images/home-testimonial-bg.jpg");
  background-position-y: center;
  background-repeat: no-repeat;
  background-size: cover;
}
.banner {
  display: flex;
  justify-content: center;
  align-items: center;
  .banner_text {
    text-align: center;

    p.author_cit {
      padding: 40px 0 170px 0;
    }
  }
  p.cit {
    font-size: 30px;
    line-height: 50px;
    padding: 170px 0 40px 0;
  }
}
</style>