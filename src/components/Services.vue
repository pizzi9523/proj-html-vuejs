<template>
  <section class="services">
    <div class="container">
      <div class="row">
        <div class="col-4" v-for="service in services" :key="service">
          <div class="service_card">
            <div class="icon_circle">
              <i :class="'fas fa-' + service.icon"></i>
            </div>
            <h4>{{ service.title }}</h4>
            <img src="../assets/images/divider-x-red.png" alt="" />
            <p>{{ service.description }}</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      services: [
        {
          icon: "dumbbell",
          title: "Strength & Conditioning",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et ullam aspernatur sequi voluptatum deleniti facilis quisquam!",
        },

        {
          icon: "bicycle",
          title: "Fitness & Cardio",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et ullam aspernatur sequi voluptatum deleniti facilis quisquam!",
        },

        {
          icon: "cloud",
          title: "Flexibility & Rest",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et ullam aspernatur sequi voluptatum deleniti facilis quisquam!",
        },

        {
          icon: "heartbeat",
          title: "Health & Diet",
          description:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Et ullam aspernatur sequi voluptatum deleniti facilis quisquam!",
        },
      ],
    };
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.services {
  background-image: url("../assets/images/gym_bkgd_bw-compressor.jpg");
  background-size: cover;
  background-position-y: center;
  padding: 100px;
  .service_card {
    text-align: center;
    .icon_circle {
      margin: auto;
      width: 80px;
      height: 80px;
      border-radius: 50%;
      color: $button-color;
      border: 1px solid $button-color;
      display: flex;
      justify-content: center;
      align-items: center;
    }
    h4 {
      font-size: 20px;
      padding: 15px 0;
    }
    p {
      color: $secondary-text-color;
      padding: 15px;
      line-height: 25px;
    }
  }
}
</style>