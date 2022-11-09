<script>
export default {
  name: "AppFooter",
  data() {
    return {
      dcComics: [
        {
          name: "Characters",
          href: "/characters",
        },
        {
          name: "Comics",
          href: "/comics",
        },
        {
          name: "Movies",
          href: "/movies",
        },
        {
          name: "Tv",
          href: "/tv",
        },
        {
          name: "Games",
          href: "/games",
        },
        {
          name: "Videos",
          href: "/videos",
        },
        {
          name: "News",
          href: "/news",
        },
      ],

      shop: [
        {
          name: "Shop DC",
          href: "/shop-dc",
        },
        {
          name: "Shop DC Collectibles",
          href: "/shop-dc-collectibles",
        },
      ],
      dc: [
        {
          name: "Terms of Use",
          href: "/terms",
        },
        {
          name: "Privacy Policy (New)",
          href: "/privacy-poliy-new",
        },
        {
          name: "Ad Choices",
          href: "/ad-choices",
        },
        {
          name: "Advertising",
          href: "/advertising",
        },
        {
          name: "Jobs",
          href: "/jobs",
        },
        {
          name: "Subscriptions",
          href: "/subscriptions",
        },
        {
          name: "Talent Workshops",
          href: "/talent-workshops",
        },
        {
          name: "CPSC Certificates",
          href: "/certificates",
        },
        {
          name: "Ratings",
          href: "/ratings",
        },
        {
          name: "Shop Help",
          href: "/shop-help",
        },
        {
          name: "Contact Us",
          href: "/contact-us",
        },
      ],
      sites: [
        {
          name: "DC",
          href: "/dc",
        },
        {
          name: "MAD Magazine",
          href: "/mad-magazine",
        },
        {
          name: "DC Universe",
          href: "/dc-universe",
        },
        {
          name: "DC Kids",
          href: "/dc-kids",
        },
        {
          name: "DC Power Visa",
          href: "/dc-power-visa",
        },
      ],
    };
  },
};
</script>

<template>
  <footer>
    <div class="footer-container">
      <div class="footer-links">
        <div class="column">
          <span>DC COMICS</span>
          <ul>
            <li v-for="item in dcComics">
              <a href="">{{ item.name }}</a>
            </li>
          </ul>
          <span>SHOP</span>
          <ul>
            <li v-for="item in shop">
              <a href="">{{ item.name }}</a>
            </li>
          </ul>
        </div>
        <div class="column">
          <span>DC</span>
          <ul>
            <li v-for="item in dc">
              <a href="">{{ item.name }}</a>
            </li>
          </ul>
        </div>
        <div class="column">
          <span>SITES</span>
          <ul>
            <li v-for="item in sites">
              <a href="">{{ item.name }}</a>
            </li>
          </ul>
        </div>
      </div>
      <div class="footer-logo"></div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
@use "../styles/partials/variables" as *;

footer {
  width: 100%;
  background-image: url("../assets/img/footer-bg.jpg");
  color: white;
  height: 300px;
  .footer-container {
    @include my-container;
    @include my-flex(row, space-between);
    height: 100%;

    .footer-links {
      padding: 1.5em;
      height: 100%;
      width: 45%;
      gap: 1em;

      @include my-flex(row, flex-start);
      align-items: flex-start;
      flex-wrap: wrap;

      .column {
        width: calc(100% / 3 - 1em);

        @include my-flex(column, flex-start);
        align-items: flex-start;
        gap: 0.5em;
        span {
          font-weight: bold;
          text-align: left;
        }
        ul {
          li {
            font-size: 0.8rem;
            color: grey;
            font-weight: 300;
            transition: 300ms;

            &:hover {
              color: white;
            }
          }
        }
      }

      .column:first-child {
        @include my-flex(column, flex-start);
        align-items: flex-start;
        gap: 0.5em;
      }
    }

    .footer-logo {
      background-image: url("../assets/img/dc-logo-bg.png");
      background-clip: border-box;
      width: 500px;
      height: 300px;
      background-clip: content-box;
      background-size: 100%;
      background-repeat: no-repeat;
      background-position: center;
    }
  }
}
</style>
