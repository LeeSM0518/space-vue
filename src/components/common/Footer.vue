<template>
  <v-footer dark padless>
    <v-card class="grey lighten-5 text-center" light flat tile width="100%">
      <v-card-text>
        <v-btn v-for="icon in icons" :key="icon" class="mx-4 mt-2" icon>
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="mb-4">
        Lorem ipsum dolor sit amet, consectetur adipisicing elit. A dicta
        doloremque eaque eos hic magnam modi molestiae, pariatur rem totam!
        Doloribus explicabo mollitia non sint! Illum natus quae quam repellat!
      </v-card-text>
      <v-divider />
      <v-card-text>
        © 2020 Hanbat Smart Human Life Design
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      icons: ["fab fa-facebook", "fab fa-instagram", "fab fa-github-alt"]
    };
  }
};
</script>

<style scoped></style>
