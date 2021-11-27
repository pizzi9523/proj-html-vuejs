<template>
  <footer class="site_footer">
    <div class="top_footer">
      <div class="container">
        <div class="row">
          <div class="col-4">
            <div class="find_us column" v-for="inf in info" :key="inf.phone">
              <h4>COME FIND US</h4>
              <p class="address">{{ inf.address }}</p>
              <p class="phone">
                Phone: <span>{{ inf.phone }}</span>
              </p>
              <p class="email">
                Email: <span>{{ inf.email }}</span>
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="recent_posts column">
              <h4>RECENT POSTS</h4>
              <p class="recent_post">
                <i class="fas fa-chevron-right"></i>
                <span>Train with free weights or your body weight?</span>
              </p>

              <p class="recent_post">
                <i class="fas fa-chevron-right"></i>
                <span>Nuritional advice that will keep you training</span>
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="openinf_times column">
              <h4>OPENING TIMES</h4>

              <div v-for="open in openingTimes" :key="open.weekday">
                <p class="weekdays">{{ open.weekday }}</p>
                <p class="time-table">{{ open.timeTable }}</p>
              </div>
            </div>
          </div>
          <div class="col-4">
            <img src="../assets/images/gym_ad-compressor.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div class="bottom_footer">
      <div class="container">
        <div class="row bottom_row_footer">
          <div class="copyright">
            <span v-for="(text, index) in copyrightText" :key="text">
              {{ text }}
              <span v-if="index != copyrightText.length - 1">|</span>
            </span>
          </div>
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
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  props: {
    info: Array,
    openingTimes: Array,
    copyrightText: Array,
  },
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.top_footer {
  background-color: $secondary-bg-color;

  padding: 80px 0;
  .column {
    margin: 0 23px;
  }
  h4 {
    font-weight: unset;
    color: $footer-text-color;
    margin-bottom: 40px;
  }
  p {
    line-height: 30px;
    color: $secondary-text-color;
    font-size: 16px;
    i {
      font-size: 11px;
      line-height: 28px;
      padding-right: 5px;
      display: block;
    }
  }
  p.time-table {
    color: $footer-text-color;
  }

  .find_us {
    span:hover {
      color: $active-text-color;
      cursor: pointer;
    }
  }

  .recent_posts {
    h4 {
      margin-bottom: 25px;
    }
  }
  p.recent_post {
    display: flex;
    padding: 15px 0;
    border-bottom: 1px solid $footer-text-color;
    span:hover {
      color: $active-text-color;
      cursor: pointer;
    }
  }
}

.bottom_footer {
  .bottom_row_footer {
    justify-content: space-between;
    align-items: center;
    .copyright {
      padding: 80px 0;
      color: $secondary-text-color;

      span {
        margin: 0 10px;
      }
    }
    .social_icon {
      background-color: $active-text-color;
    }
  }
}
</style>