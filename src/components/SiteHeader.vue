<template>
  <header>
    <div class="logo">
      <img
        width="180"
        height="96"
        src="../assets/images/gym_logo_1x.png"
        alt=""
      />
    </div>
    <nav>
      <ul>
        <li
          v-for="(option, index) in navMenu"
          :key="option"
          :class="active != index ? '' : 'active'"
          @click="active = index"
        >
          <a href="#">{{ option.toUpperCase() }}</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {
  data() {
    return {
      active: 0,
    };
  },
  props: {
    navMenu: Array,
  },
};
</script>


<style lang="scss">
@import "../assets/scss/variables.scss";

header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 40px 133px 0px 133px;
  background-color: black;

  nav {
    color: $primary-text-color;
    ul {
      display: flex;
      list-style: none;
      li {
        margin: 0 1rem;
        &.active {
          a {
            color: $active-text-color;
          }
        }
        a {
          transition: 0.5s;
          text-decoration: none;
          color: $primary-text-color;
          font-size: 13px;
          &:hover {
            color: $active-text-color;
          }
        }
      }
    }
  }
}
</style>