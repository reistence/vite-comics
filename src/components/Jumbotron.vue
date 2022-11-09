<script>
export default {
  name: "Jumbotron",
  props: {
    imgSrc: String,
  },
};
</script>

<template>
  <div class="container-fluid">
    <img :src="imgSrc" alt="" />
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

.container-fluid {
  width: 100%;
}
</style>
