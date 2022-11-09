<script>
export default {
  name: "AppCard",
  props: {
    name: String,
    imgSrc: String,
  },
};
</script>

<template>
  <div class="card">
    <div class="card-img">
      <img :src="imgSrc" :alt="name" />
    </div>
    <div class="card-txt">
      <p>{{ name }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;
.card {
  width: calc(100% / 6 - 1em);
  padding: 0.5em;

  @include my-flex(column, space-between);
  gap: 0.5em;

  .card-img {
    width: 100%;

    img {
      object-fit: cover;
    }
  }
  .card-txt {
    p {
      color: white;
      font-size: 0.6rem;
      text-transform: uppercase;
    }
  }
}
</style>
