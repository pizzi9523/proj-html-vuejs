<template>
  <section class="results">
    <SectionTitle title="REAL WORLD RESULTS" />
    <div class="container">
      <div class="row">
        <div class="col-6" v-for="review in reviews" :key="review.id">
          <div class="review_card">
            <img
              height="160"
              :src="
                require(`../assets/images/review_${review.id}-compressor.jpg`)
              "
              alt=""
            />
            <div>
              <p>{{ review.text }}</p>
              <p>- {{ review.reviewer }}</p>
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
      reviews: [
        {
          id: 1,
          text: '"The trainers Avada Gym have helped me reach my fitness goals beyond anything i could of hoped for. I love it!"',
          reviewer: "Tara Smith",
        },

        {
          id: 2,
          text: '"The atmosphere at Avada Gym is amazing, the people are even better. All in all, it is a great place to work out."',
          reviewer: "Simon Chel",
        },

        {
          id: 3,
          text: '"The facilities at Avada Gym stood out to me the most. They are well maintained and have high quality equipment."',
          reviewer: "Jen Wirth",
        },

        {
          id: 4,
          text: '"No bad things to say about Avada Gym, they are top notch at every corner and truly take care of their customers."',
          reviewer: "Jeff Glum",
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

.results {
  background-color: $secondary-bg-color;
  padding-bottom: 200px;
  .section_title {
    padding-bottom: 20px;
  }
  .review_card {
    background-color: $primary-bg-color;
    margin: 15px;
    padding: 25px;
    display: flex;
    gap: 25px;
    p {
      padding: 10px 0;
      line-height: 30px;
      color: $secondary-text-color;
    }
  }
}
</style>