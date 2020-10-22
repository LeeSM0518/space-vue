<template>
  <v-container fluid class="mt-4">
    <v-row>
      <v-col v-for="i in 9" :key="i" cols="12" sm="4">
        <v-img
          :src="`https://picsum.photos/500/300?image=${i * 5 + 10}`"
          :lazy-src="`https://picsum.photos/10/6?image=${i * 5 + 10}`"
          aspect-ratio="1"
        ></v-img>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Pictures"
};
</script>

<style scoped></style>
