<template>
  <section class="services">
    <div class="container">
      <div class="row">
        <div class="col-4" v-for="service in services" :key="service.title">
          <div class="service_card">
            <div class="icon_circle">
              <i :class="'fas fa-' + service.icon + ' fa-2x'"></i>
              <div class="icon_circle_effect"></div>
            </div>
            <!-- /.icon_circle  -->
            <h4>{{ service.title }}</h4>
            <img src="../assets/images/divider-x-red.png" alt="" />
            <p>{{ service.description }}</p>
          </div>
          <!-- /.service_card  -->
        </div>
        <!-- /.col-4  -->
      </div>
      <!-- /.row  -->
    </div>
    <!-- /.container  -->
  </section>
  <!-- /.services  -->
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
  padding: 120px;
  .service_card {
    text-align: center;

    img {
      filter: hue-rotate($image-hue-rotate);
    }

    .icon_circle_effect {
      position: absolute;
      width: 145px;
      height: 145px;
      border-radius: 50%;
      border: 15px solid $primary-theme-color;
      animation: pulse-ring 2s cubic-bezier(0.215, 0.61, 0.355, 1) 1;
      display: none;
    }
    .icon_circle {
      margin: auto;
      width: 80px;
      height: 80px;
      border-radius: 50%;
      color: $primary-theme-color;
      border: 1px solid $primary-theme-color;
      display: flex;
      justify-content: center;
      align-items: center;
      transition: 0.9s;

      &:hover {
        transform: scale(0.9);
        cursor: pointer;
        .icon_circle_effect {
          display: block;
          opacity: 0;
        }

        & + h4 {
          color: $primary-theme-color;
          transition: 0.5s;
        }
      }
    }
    @keyframes pulse-ring {
      0% {
        transform: scale(0.66);
        opacity: 0.8;
      }
      80%,
      100% {
        opacity: 0;
      }
    }
    h4 {
      font-size: 16px;
      padding: 15px 0;
    }
    p {
      color: $secondary-text-color;
      padding: 15px;
      line-height: 30px;
      font-size: 12px;
    }
  }
}
</style>