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
    <img :src="getImgPath(`../assets/img/${imgSrc}`)" alt="" />
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container-fluid {
  width: 100%;
  img {
    display: block;
  }
}
</style>
