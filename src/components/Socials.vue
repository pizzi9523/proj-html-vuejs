<template>
  <div class="socials">
    <div class="social_icon">
      <i class="fab fa-facebook-f"></i>
    </div>
    <div class="social_icon">
      <i class="fab fa-twitter"></i>
    </div>
    <div class="social_icon">
      <i class="fab fa-instagram"></i>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.socials {
  display: flex;
  gap: 10px;

  .social_icon {
    width: 50px;
    height: 50px;
    text-align: center;
    line-height: 50px;
  }
}
</style>