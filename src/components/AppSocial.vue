<script>
export default {
  name: "AppHeader",
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
    border: 1px solid green;
    @include my-flex(row, space-between);
    button {
      color: white;
      border: 2px solid $blue;
      background-color: rgb(49, 46, 46);
      padding: 1em;
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
