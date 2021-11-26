<template>
  <section class="trainers">
    <SectionTitle title="MEET OUR TRAINERS" />
    <div class="container">
      <div class="row">
        <div class="col-3" v-for="trainer in trainers" :key="trainer.id">
          <div class="trainer_card">
            <div class="card_img_wrapper">
              <img
                :src="
                  require(`../assets/images/trainer${trainer.id}-400x297.jpg`)
                "
                alt=""
              />
            </div>

            <div class="body_card">
              <h4>{{ trainer.name }}</h4>
              <h3>{{ trainer.role }}</h3>
              <p>
                {{ trainer.description }}
              </p>
              <div class="socials_trainer">
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
            </div>
          </div>
        </div>
      </div>
      <div class="button">
        <button class="button_light">VIEW ALL TRAINERS</button>
      </div>
    </div>
  </section>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";

export default {
  data() {
    return {
      trainers: [
        {
          id: 1,
          name: "Anna Baker",
          role: "Personal Trainer",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam explicabo.",
        },

        {
          id: 2,
          name: "Anne Warren",
          role: "Personal Trainer",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam explicabo.",
        },

        {
          id: 3,
          name: "Peter Rice",
          role: "Personal Trainer",
          description:
            "Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam explicabo.",
        },
      ],
    };
  },
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.trainer_card {
  background-color: $secondary-bg-color;

  .card_img_wrapper {
    opacity: 1;
    transform: scale(1);
    transition: transform 0.35s;
    &:hover {
      transform: scale(1.03);
      cursor: pointer;
      img {
        box-shadow: 0px 0px 25px black;
      }
    }
    img {
      width: 100%;
      transition: all 0.35s;
    }
  }

  .body_card {
    background-color: $secondary-bg-color;
    padding: 40px;
    h3 {
      padding: 10px 0;
      font-size: 16px;
    }
    p {
      padding: 28px 0;
      line-height: 35px;
      color: $secondary-text-color;
    }

    .socials_trainer {
      display: flex;
      gap: 10px;

      .social_icon {
        width: 50px;
        height: 50px;
        text-align: center;
        line-height: 50px;
        background-color: $primary-bg-color;
        border-radius: 10px;
        &:hover {
          cursor: pointer;
          color: $active-text-color;
        }
      }
    }
  }
}

.button {
  text-align: center;
  padding: 50px;
}
</style>