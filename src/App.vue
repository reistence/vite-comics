<script>
import AppHeader from "./components/AppHeader.vue";
import AppMainContent from "./components/AppMainContent.vue";
import FooterBanner from "./components/FooterBanner.vue";
import AppFooter from "./components/AppFooter.vue";
import AppSocial from "./components/AppSocial.vue";

export default {
  components: {
    AppHeader,
    AppMainContent,
    FooterBanner,
    AppFooter,
    AppSocial,
  },
};
</script>

<template>
  <AppHeader></AppHeader>
  <AppMainContent></AppMainContent>
  <FooterBanner></FooterBanner>
  <AppFooter></AppFooter>
  <AppSocial></AppSocial>
</template>

<style lang="scss">
@use "./styles/general.scss" as *;
</style>
