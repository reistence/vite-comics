<script>
export default {
  name: "AppSocialBanner",
  data() {
    return {};
  },
};
</script>

<template>
  <div>
    <div class="container">
      <button>SIGN-UP NOW!</button>
      <ul>
        <span>FOLLOW US</span>
        <li>
          <a href=""><img src="../assets/img/footer-facebook.png" alt="" /></a>
        </li>
        <li>
          <a href=""><img src="../assets/img/footer-twitter.png" alt="" /></a>
        </li>
        <li>
          <a href=""><img src="../assets/img/footer-youtube.png" alt="" /></a>
        </li>
        <li>
          <a href=""><img src="../assets/img/footer-pinterest.png" alt="" /></a>
        </li>
        <li>
          <a href=""><img src="../assets/img/footer-periscope.png" alt="" /></a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

div {
  width: 100%;
  height: 80px;
  background-color: rgb(49, 46, 46);
  .container {
    @include my-container;
    height: 80px;

    @include my-flex(row, space-between);
    button {
      color: white;
      border: 2px solid $blue;
      background-color: rgb(49, 46, 46);
      padding: 1em;
      transition: 300ms;

      &:hover {
        background-color: $blue;
        border: 2px solid white;
      }
    }

    @media screen and (max-width: 780px) {
      button {
        padding: 0.5em;
        margin-right: 0.4em;
      }
    }
    @media screen and (max-width: 480px) {
      button {
        padding: 0.3em;
        margin-right: 0.4em;
      }
    }

    ul {
      @include my-flex(row, space-around);
      gap: 1em;
      span {
        color: $blue;
        font-weight: bold;
      }
    }
  }
}
</style>
