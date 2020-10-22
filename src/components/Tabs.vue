<template>
  <v-container>
    <v-tabs color="black" grow>
      <v-tab>
        자기소개
      </v-tab>
      <v-tab-item>
        <Introduction />
      </v-tab-item>

      <v-tab>
        작품사진
      </v-tab>
      <v-tab-item>
        <Pictures />
      </v-tab-item>

      <v-tab>
        다이어리
      </v-tab>
      <v-tab-item>
        <Diary />
      </v-tab-item>
    </v-tabs>

    <v-dialog v-model="dialog" persistent width="40%" max-width="400px">
      <v-card>
        <v-card-title>
          <span class="headline ma-1">로그인</span>
        </v-card-title>
        <v-card-text>
          <v-text-field label="아이디"></v-text-field>
          <v-text-field label="비밀번호" type="password"></v-text-field>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="blue" dark class="ma-4" @click="dialog = false">
            <b>로그인</b>
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-dialog>
  </v-container>
</template>

<script>
import Diary from "@/components/Diary";
import Pictures from "@/components/Pictures";
import Introduction from "@/components/Introduction";

export default {
  name: "Tabs",
  components: {
    Introduction,
    Diary,
    Pictures
  },
  data() {
    return {
      dialog: true
    };
  }
};
</script>

<style scoped></style>
