<script>
export default {
  name: "Jumbotron",
  props: {
    imgSrc: String,
  },
  methods: {
    getImgPath(imgPath) {
      return new URL(imgPath, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="container-fluid">
    <div>
      <img :src="getImgPath(`../assets/img/${imgSrc}`)" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container-fluid {
  width: 100%;

  div {
    width: 100%;
    height: 300px;
    overflow: hidden;

    img {
      display: block;
      object-fit: fill;
    }
  }
  @media screen and (max-width: 780px) {
    .div {
      height: 100%;
    }
    img {
      object-fit: cover !important;
    }
  }

  @media screen and (max-width: 480px) {
    .div {
      height: 100%;
    }
    img {
      object-fit: cover !important;
      height: 100% !important;
    }
  }
}
</style>
