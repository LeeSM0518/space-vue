<template>
  <v-app-bar fixed class="grey lighten-5 px-md-8">
    <v-toolbar-title
      ><span class="logo mx-6">Yourstagram</span></v-toolbar-title
    >
    <v-spacer></v-spacer>

    <v-btn icon>
      <v-icon color="black">fal fa-user</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon color="black">fal fa-images</v-icon>
    </v-btn>
    <v-btn icon>
      <v-icon color="black">fal fa-book</v-icon>
    </v-btn>

    <v-avatar size="28" class="mx-2">
      <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
    </v-avatar>
  </v-app-bar>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style scoped>
.logo {
  font-family: "Lemon Jelly Personal Use", serif;
  font-size: 2.4rem;
}
</style>
