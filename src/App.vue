<template>
  <v-app>
    <Header />
    <Profile />
    <Tabs />
    <Footer />
  </v-app>
</template>

<script>
import Header from "@/components/common/Header";
import Footer from "@/components/common/Footer";
import Profile from "@/components/Profile";
import Tabs from "@/components/Tabs";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Profile,
    Tabs
  }
};
</script>
<style>
@font-face {
  font-family: "Lemon Jelly Personal Use";
  src: local("Lemon Jelly Personal Use"),
    url(~@/assets/fonts/insta-font.ttf) format("truetype");
}

$material-light: (
  "background": #fff
);
</style>
