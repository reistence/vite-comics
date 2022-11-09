<script>
export default {
  name: "FooterBanner",
  data() {
    return {
      items: [
        {
          name: "DIGITAL COMICS",
          //   img: "../asset/img/buy-comics-digital-comics.png",
          img: "buy-comics-digital-comics.png",
        },
        {
          name: "DC MERCHANDISE",
          img: "buy-comics-merchandise.png",
        },
        {
          name: "SUBSCRIPTION",
          img: "buy-comics-subscriptions.png",
        },
        {
          name: "COMIC SHOP LOCATOR",
          img: "buy-comics-shop-locator.png",
        },
        {
          name: "DC POWER VISA",
          img: "buy-dc-power-visa.svg",
        },
      ],
    };
  },
  methods: {
    getImgPath(imgPath) {
      return new URL(imgPath, import.meta.url).href;
    },
  },
};
</script>

<template>
  <div class="footer-banner">
    <div class="footer-banner-container">
      <ul>
        <li v-for="item in items">
          <div>
            <img
              :src="getImgPath(`../assets/img/${item.img}`)"
              :alt="item.name"
            />
          </div>
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

    ul {
      height: 100%;
      @include my-flex(row, space-around);

      li {
        @include my-flex(row, space-between);

        gap: 0.4em;
        flex-wrap: wrap;
        div {
          width: 40px;
        }

        img {
          object-fit: contain;
          width: 40px;
          height: 40px;
        }
        a {
          font-size: 0.8rem;
          color: white;
          min-width: max-content;
        }
        @media screen and (max-width: 780px) {
          a {
            display: none;
          }
        }

        @media screen and (max-width: 480px) {
          a {
            display: none;
          }
        }
      }
    }
  }
}
</style>
