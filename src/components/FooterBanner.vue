<script>
export default {
  name: "FooterBanner",
  data() {
    return {
      items: [
        {
          name: "DIGITAL COMICS",
          img: "../asset/img/buy-comics-digital-comics.png",
        },
        {
          name: "DC MERCHANDISE",
          img: "./asset/img/buy-comics-merchandise.png",
        },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-banner">
    <div class="footer-banner-container">
      <ul>
        <li v-for="item in items">
          <img src="`{{item.img}}`" :alt="item.name" />
          <a href="">{{ item.name }}</a>
        </li>
      </ul>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.footer-banner {
  width: 100%;
  background-color: $blue;
  height: 150px;

  .footer-banner-container {
    height: 150px;
    @include my-container;
    border: 1px solid red;
  }
}
</style>
