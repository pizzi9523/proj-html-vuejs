<template>
  <section class="sign_up">
    <div class="world_class">
      <div class="triangle"></div>

      <SectionTitle
        title="WORLD CLASS Fitness"
        text="At Avada Gym, everything we do from top to bottom is of the heighest
      quality to ensure we're equipped to help you reach your goals of a healthly and fit lifestyle"
      />
    </div>
    <!-- /.world_class  -->

    <div class="sign_up_form">
      <div class="container">
        <div class="row">
          <div class="col-6">
            <img src="../assets/images/home_img-compressor.jpg" alt="" />
          </div>
          <div class="col-6">
            <form class="form_signup">
              <h3>Sign Up For A Free Training Session!</h3>

              <label for="name">Name</label>
              <input type="text" name="username" id="name" />
              <label for="email">Email</label>
              <input type="email" name="email" id="email" />
              <button>START NOW!</button>
            </form>
            <!-- /.form_signup -->
          </div>
          <!-- /.col-6  -->
        </div>
        <!-- /.row  -->
      </div>
      <!-- /.container  -->
    </div>
    <!-- /.sign_up_form  -->
  </section>
  <!-- /.sign_up  -->
</template>

<script>
import SectionTitle from "./SectionTitle.vue";
export default {
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.sign_up {
  .world_class {
    background-color: $secondary-bg-color;
    position: relative;
    .triangle {
      bottom: -50px;
      left: 50%;
      background-color: $secondary-bg-color;
    }
  }
  .sign_up_form {
    background-color: $primary-bg-color;
    padding: 100px;
    img {
      width: 100%;
    }

    .form_signup {
      padding: 0 40px;
      display: flex;
      flex-direction: column;
      gap: 15px;

      h3 {
        font-size: 25px;
        margin-bottom: 40px;
      }

      label {
        color: $secondary-text-color;
      }
      input {
        background-color: transparent;
        border: 1px solid $secondary-text-color;
        padding: 16px;
        margin-bottom: 20px;
        color: $secondary-text-color;
      }
      button {
        padding: 20px 10px;
        background-color: $button-color;
        border: none;
        color: $primary-text-color;
        &:hover {
          cursor: pointer;
          filter: brightness(0.8);
        }
      }
    }
  }
}
</style>