<script>
export default {
  name: "AppHeader",
  data() {
    return {
      headerLinks: [
        {
          name: "CHARACTERS",
          link: "/characters",
          active: false,
        },
        {
          name: "COMICS",
          link: "/comics",
          active: true,
        },
        {
          name: "MOVIES",
          link: "/movies",
          active: false,
        },
        {
          name: "TV",
          link: "/tv",
          active: false,
        },
        {
          name: "GAMES",
          link: "/games",
          active: false,
        },
        {
          name: "COLLECTIBLES",
          link: "/collectibles",
          active: false,
        },
        {
          name: "VIDEOS",
          link: "/videos",
          active: false,
        },
        {
          name: "FANS",
          link: "/fans",
          active: false,
        },
        {
          name: "NEWS",
          link: "/news",
          active: false,
        },
        {
          name: "SHOP",
          link: "/shop",
          active: false,
        },
      ],
    };
  },
};
</script>

<template>
  <header>
    <div class="header-container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="" />
      </div>
      <ul>
        <li
          :class="{ active: link.active }"
          v-for="(link, index) in headerLinks"
        >
          <a :href="link.link">{{ link.name }}</a>
        </li>
      </ul>
    </div>
  </header>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

header {
  width: 100%;
  height: 100px;

  .header-container {
    height: 100%;
    @include my-container;

    @include my-flex(row, space-between);
    .logo {
      height: 100%;
      padding: 1em;
      img {
        height: 100%;
        object-fit: cover;
      }
    }

    ul {
      height: 100%;
      @include my-flex(row, space-around);
      gap: 1em;

      li {
        font-size: 0.8rem;
        font-weight: bold;
        line-height: 100px;
        &.active {
          color: $blue;
        }
        &:hover {
          color: $blue;
        }
      }
    }
  }
}
</style>
