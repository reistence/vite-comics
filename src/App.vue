<script>
import AppHeader from "./components/AppHeader.vue";
import AppMainContent from "./components/AppMainContent.vue";
import FooterBanner from "./components/FooterBanner.vue";
import AppFooter from "./components/AppFooter.vue";
import AppSocialBanner from "./components/AppSocialBanner.vue";
import AppCard from "./components/AppCard.vue";
import Jumbotron from "./components/Jumbotron.vue";

export default {
  components: {
    AppHeader,
    AppMainContent,
    AppCard,
    FooterBanner,
    AppFooter,
    AppSocialBanner,
    Jumbotron,
  },
};
</script>

<template>
  <AppHeader></AppHeader>
  <Jumbotron :imgSrc="`./assets/img/jumbotron.jpg`"></Jumbotron>
  <AppMainContent></AppMainContent>
  <FooterBanner></FooterBanner>
  <AppFooter></AppFooter>
  <AppSocialBanner></AppSocialBanner>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
