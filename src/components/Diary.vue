<template>
  <v-container fluid class="mt-4" style="min-height: 600px">
    <v-row justify="center">
      <v-col cols="3">
        <v-menu
          ref="menu"
          v-model="menu"
          :close-on-content-click="false"
          transition="scale-transition"
          offset-y
        >
          <template v-slot:activator="{ on, attrs }">
            <v-text-field
              v-model="date"
              prepend-inner-icon="mdi-calendar"
              color="black"
              readonly
              placeholder="날짜"
              v-bind="attrs"
              v-on="on"
            ></v-text-field>
          </template>
          <v-date-picker
            ref="picker"
            v-model="date"
            :max="new Date().toISOString().substr(0, 10)"
            min="1950-01-01"
            @change="save"
            color="black"
          ></v-date-picker>
        </v-menu>
      </v-col>

      <v-col cols="6">
        <v-textarea
          placeholder="오늘의 메모"
          color="black"
          v-model="content"
          rows="1"
          auto-grow
          clearable
        ></v-textarea>
      </v-col>
      <v-col cols="2">
        <v-btn class="mx-auto" fab light outlined @click="saveDiary">
          <v-icon small>
            fs fa-pen
          </v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col v-for="elem in diary" :key="elem.id" cols="6" sm="4">
        <v-card class="mx-auto" outlined>
          <v-list-item three-line>
            <v-list-item-content>
              <div class="overline mb-4">
                {{ elem.date }}
              </div>
              <v-card-text class="headline mb-1">
                {{ elem.content }}
              </v-card-text>
            </v-list-item-content>
          </v-list-item>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Diary",
  data: () => ({
    diary: [],
    content: "",
    date: null,
    menu: false
  }),
  watch: {
    menu(val) {
      val && setTimeout(() => (this.$refs.picker.activePicker = "YEAR"));
    }
  },
  methods: {
    save(date) {
      this.$refs.menu.save(date);
    },
    saveDiary() {
      this.diary.push({
        id: this.diary.length,
        content: this.content,
        date: this.date
      });
      this.content = "";
      this.date = null;
    }
  }
};
</script>

<style scoped></style>
