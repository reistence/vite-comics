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
  transition: 300ms;

  &:hover {
    transform: scale(1.08);
  }

  .card-img {
    width: 100%;

    img {
      object-fit: cover;
    }
  }
  .card-txt {
    p {
      color: white;
      font-size: 0.8rem;
      text-transform: uppercase;
    }
  }
}

@media screen and (max-width: 780px) {
  .card {
    width: calc(100% / 4 - 1em);
  }
}

@media screen and (max-width: 660px) {
  .card {
    width: calc(100% / 3 - 1em);
  }
}

@media screen and (max-width: 480px) {
  .card {
    width: calc(100% / 2 - 1em);
  }
}
</style>
