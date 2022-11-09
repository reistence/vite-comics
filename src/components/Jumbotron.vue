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
}
</style>
