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
      hamMenu: false,
    };
  },
  methods: {
    showHamMenu() {
      this.hamMenu = !this.hamMenu;
    },
  },
};
</script>

<template>
  <header>
    <div class="header-container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="" />
      </div>
      <div @click="showHamMenu" class="ham-menu">
        <i class="fa-solid fa-bars"></i>

        <ul class="menu" :class="hamMenu === true ? 'active' : ''">
          <li
            class="menu-item"
            :class="{ active: link.active }"
            v-for="(link, index) in headerLinks"
          >
            <a :href="link.link">{{ link.name }}</a>
          </li>
        </ul>
      </div>
      <ul>
        <li
          class="header-item"
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
    .ham-menu {
      display: none;
      position: relative;
    }
    ul {
      height: 100%;
      @include my-flex(row, space-around);
      gap: 1em;
      width: 60%;

      .header-item {
        font-size: 0.8rem;
        font-weight: bold;
        line-height: 100px;
        position: relative;

        &.active {
          color: $blue;

          &::after {
            content: "";
            position: absolute;
            bottom: 0%;
            left: 0;
            height: 5px;
            width: 100%;
            background-color: $blue;
          }
        }
        &:hover {
          color: $blue;
          transition: all 300ms ease;

          &::after {
            content: "";
            position: absolute;
            bottom: 0%;
            left: 0;
            height: 5px;
            width: 100%;
            background-color: $blue;
            animation: height 300ms ease;
          }
          @keyframes height {
            0% {
              height: 0px;
            }
            50% {
              height: 3px;
            }
            100% {
              height: 5px;
            }
          }
        }
      }
    }
  }
}

@media screen and (max-width: 880px) {
  header {
    .header-container {
      .ham-menu {
        display: block;

        .menu {
          display: none;
          border-radius: 10px;
          flex-direction: column;
          justify-content: flex-start;
          align-items: flex-start;
          background-color: $blue;
          height: 270px;
          gap: 0.5em;
          width: 120px;
          color: white;
          padding: 1em;
          position: absolute;
          top: 23px;
          left: -105px;

          &.active {
            display: flex;
          }
          .menu-item {
            line-height: normal;
            font-size: 0.8rem;
            font-weight: bold;
            transition: 300ms;

            &:hover {
              color: black;
            }
          }
        }
      }
      ul {
        display: none;
      }
    }
  }
}

@media screen and (max-width: 480px) {
  header {
    .header-container {
      .ham-menu {
        display: block;

        .menu {
          display: none;
          border-radius: 10px;
          flex-direction: column;
          justify-content: flex-start;
          align-items: flex-start;
          background-color: $blue;
          height: 270px;
          gap: 0.5em;
          width: 120px;
          color: white;
          padding: 1em;
          position: absolute;
          top: 23px;
          left: -105px;

          &.active {
            display: flex;
          }
          .menu-item {
            line-height: normal;
            font-size: 0.8rem;
            font-weight: bold;
            transition: 300ms;

            &:hover {
              color: black;
            }
          }
        }
      }
      ul {
        display: none;
      }
    }
  }
}
</style>
