<template>
  <section class="performance_news">
    <SectionTitle title="PERFORMANCE NEWS" />
    <div class="container">
      <div class="row">
        <div v-for="news in blog" :key="news.title" class="col-3">
          <div class="card_news">
            <div class="card_img_wrapper">
              <img :src="require(`../assets/images/${news.img}.jpg`)" alt="" />
              <div class="wrapper_parallax">
                <i class="fas fa-link fa-2x"></i>
                <i class="fas fa-search fa-2x"></i>
              </div>
            </div>

            <div class="body_card">
              <h2>{{ news.title }}</h2>
              <p>
                {{ news.content.substr(0, 90) + " [...]" }}
              </p>
            </div>
          </div>

          <div class="card_news">
            <div class="card_img_wrapper">
              <img
                :src="require(`../assets/images/${news.img_1}.jpg`)"
                alt=""
              />
              <div class="wrapper_parallax">
                <i class="fas fa-link fa-2x"></i>
                <i class="fas fa-search fa-2x"></i>
              </div>
            </div>

            <div class="body_card">
              <h2>{{ news.title_1 }}</h2>
              <p>
                {{ news.content_1.substr(0, 90) + " [...]" }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import SectionTitle from "./SectionTitle.vue";

export default {
  data() {
    return {
      blog: [
        {
          title: "Train with free weights or your body weight?",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img: "blog1",

          title_1: "To be number one, train like you're number two",
          content_1:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img_1: "blog4-400x289",
        },

        {
          title: "Nutritional advice thet will keep you training",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img: "blog6-400x400",

          title_1: "Top 5 mistakes every gym member makes",
          content_1:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img_1: "trainer2-600x445",
        },

        {
          title: "Simple principles for your next workout",
          content:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img: "trainer3",

          title_1: "The myths of shedding body fat explored",
          content_1:
            "Lorem ipsum dolor sit amet consectetur adipisicing elit. Quidem sunt labore minus incidunt doloribus saepe quibusdam ut quo,sapiente voluptatibus earum deleniti, numquam animi ex consequatur eligendi aliquam perferendis repellat. Quibusdam eius molestiae ipsa non fuga quis, natus obcaecati dolorum, tempora reprehenderit quia maxime quisquam numquam nostrum quae fugiat corporis.",
          img_1: "trainer1",
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

.performance_news {
  background-color: $secondary-bg-color;

  .card_news {
    background-color: $primary-bg-color;
    margin: 15px;

    .card_img_wrapper {
      position: relative;
      &:hover {
        cursor: pointer;
        .wrapper_parallax {
          width: 100%;
        }
      }
      img {
        width: 100%;
      }
    }
    .wrapper_parallax {
      background-image: url("../assets/images/home-parallax.jpg");
      background-size: 100% 100%;
      filter: hue-rotate(90deg);
      width: 0;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      position: absolute;
      top: 0;
      left: 0;
      opacity: 0.8;
      transition: 0.5s;
      overflow: hidden;

      i {
        opacity: 1;
      }
    }
  }

  .body_card {
    background-color: $primary-bg-color;

    padding: 20px 30px;
    h2 {
      padding: 20px 0;
    }

    p {
      line-height: 35px;
      color: $secondary-text-color;
    }
  }
}
</style>