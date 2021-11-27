<template>
  <section class="performance_news">
    <div class="triangle"></div>
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
              <!-- /.wrapper_parallax -->
            </div>
            <!-- /.card_img_wrapper -->

            <div class="body_card">
              <h2>{{ news.title }}</h2>
              <p>
                {{ news.content.substr(0, 90) + " [...]" }}
              </p>
            </div>
            <!-- /.body_card  -->
          </div>
          <!-- /.card_news  -->

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
              <!-- /.wrapper_parallax -->
            </div>
            <!-- /.card_img_wrapper -->

            <div class="body_card">
              <h2>{{ news.title_1 }}</h2>
              <p>
                {{ news.content_1.substr(0, 90) + " [...]" }}
              </p>
            </div>
            <!-- /.body_card  -->
          </div>
          <!-- /.card_news  -->
        </div>
        <!-- /.col-3  -->
      </div>
      <!-- /.row  -->
      <div class="button">
        <button class="button_light">READ ALL ARTICLES</button>
      </div>
    </div>
    <!-- /.container  -->
  </section>
  <!-- /.performance_news  -->
</template>

<script>
import SectionTitle from "./SectionTitle.vue";

export default {
  props: {
    blog: Array,
  },
  data() {
    return {};
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
  padding-bottom: 80px;
  .triangle {
    background-color: $primary-bg-color;
    left: 50%;
  }

  .card_news {
    background-color: $primary-bg-color;
    margin: 15px;

    .card_img_wrapper {
      position: relative;
      &:hover {
        cursor: pointer;
        .wrapper_parallax {
          width: 100%;
          opacity: 0.9;
        }
      }
      img {
        width: 100%;
      }
    }
    .wrapper_parallax {
      background-color: $active-text-color;
      width: 0;
      height: 100%;
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 20px;
      position: absolute;
      top: 0;
      left: 0;
      opacity: 0;
      transition: 0.6s;
      overflow: hidden;
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