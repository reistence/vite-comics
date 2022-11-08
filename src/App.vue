<script>
import AppHeader from "./components/AppHeader.vue";
import AppMainContent from "./components/AppMainContent.vue";
import FooterBanner from "./components/FooterBanner.vue";
import AppFooter from "./components/AppFooter.vue";
import AppSocialBanner from "./components/AppSocialBanner.vue";

export default {
  components: {
    AppHeader,
    AppMainContent,
    FooterBanner,
    AppFooter,
    AppSocialBanner,
  },
};
</script>

<template>
  <AppHeader></AppHeader>
  <AppMainContent></AppMainContent>
  <FooterBanner></FooterBanner>
  <AppFooter></AppFooter>
  <AppSocialBanner></AppSocialBanner>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
