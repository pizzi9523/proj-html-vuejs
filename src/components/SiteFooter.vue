<template>
  <footer class="site_footer">
    <div class="top_footer">
      <div class="container">
        <div class="row">
          <div class="col-4">
            <div class="column">
              <h4>COME FIND US</h4>
              <div class="find_us" v-for="inf in info" :key="inf.phone">
                <p class="address">{{ inf.address }}</p>
                <p class="phone">
                  Phone: <span>{{ inf.phone }}</span>
                </p>
                <p class="email">
                  Email: <span>{{ inf.email }}</span>
                </p>
              </div>
            </div>
          </div>
          <div class="col-4">
            <div class="recent_posts column">
              <h4>RECENT POSTS</h4>
              <p
                class="recent_post"
                v-for="(post, index) in blog"
                :key="post.img"
                v-show="index < 2"
              >
                <i class="fas fa-chevron-right"></i>
                <span>{{ post.title }}</span>
              </p>
            </div>
          </div>
          <div class="col-4">
            <div class="column">
              <h4>OPENING TIMES</h4>

              <div
                class="opening_times"
                v-for="open in openingTimes"
                :key="open.weekday"
              >
                <p class="weekdays">Weekdays {{ open.weekday }}</p>
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
              <span class="divider" v-if="index != copyrightText.length - 1"
                >|</span
              >
            </span>
          </div>
          <Socials />
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
import Socials from "./Socials.vue";
export default {
  props: {
    info: Array,
    openingTimes: Array,
    copyrightText: Array,
    blog: Array,
  },
  components: {
    Socials,
  },
};
</script>

<style lang="scss">
@import "../assets/scss/variables.scss";

.top_footer {
  background-color: $secondary-bg-color;
  padding: 80px 0;
  .column {
    margin-right: 23px;
    .find_us {
      margin-bottom: 20px;
    }
    .opening_times {
      margin-bottom: 24px;
    }
  }
  h4 {
    font-weight: unset;
    color: $footer-text-color;
    margin-bottom: 40px;
  }
  p {
    line-height: 30px;
    color: $secondary-text-color;
    font-size: 14px;
    i {
      font-size: 9px;
      line-height: 30px;
      padding-right: 5px;
      display: block;
    }
  }
  p.time-table {
    color: $footer-text-color;
  }

  .find_us {
    span:hover {
      color: $primary-theme-color;
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
      color: $primary-theme-color;
      cursor: pointer;
    }
  }
}

.bottom_footer {
  .bottom_row_footer {
    justify-content: space-between;
    align-items: center;
    .copyright {
      font-size: 12px;
      padding: 80px 0;
      color: $secondary-text-color;

      span.divider {
        margin: 0 10px;
      }
    }
    .social_icon {
      background-color: $primary-theme-color;
    }
  }
}
</style>