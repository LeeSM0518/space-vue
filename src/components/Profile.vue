<template>
  <v-container class="mt-4">
    <v-row align="center" justify="center" class="mt-10">
      <v-avatar size="168" class="mx-12">
        <img src="https://cdn.vuetifyjs.com/images/john.jpg" alt="John" />
      </v-avatar>
      <v-col class="mt-5" sm="7">
        <p class="text-h5">{ Your name }</p>
        <div class="mt-4">
          <span class="text-subtitle-1 mr-16">생일<b> 2020.10.21</b></span>
          <span class="text-subtitle-1 mr-8">학과<b> 산업디자인학과</b></span>
        </div>
        <div class="mt-2">
          <span class="text-subtitle-1 mr-8">번호<b> 010-0000-0000</b></span>
          <span class="text-subtitle-1 mr-8"
            >이메일<b> hello@wisoft.io</b></span
          >
        </div>
        <div class="mt-4"></div>
        <p class="text-subtitle-1 mt-4">
          Lorem ipsum dolor sit amet, consectetur adipisicing elit. Aliquam,
          repudiandae!
        </p>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Profile",

  data: () => ({
    dialog: true
  })
};
</script>
