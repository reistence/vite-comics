<script>
export default {
  name: "AppMainContent",
  data() {
    return {};
  },
};
</script>

<template>
  <main>
    <div class="main-container">
      <div>
        <h1>CONTENT GOES HERE</h1>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

main {
  background-color: black;
  height: 200px;

  .main-container {
    @include my-container;
    border: 1px solid white;
    height: 100%;
    div {
      @include my-flex(row, center);
      align-items: center;
      height: 100%;
      h1 {
        color: white;
      }
    }
  }
}
</style>
