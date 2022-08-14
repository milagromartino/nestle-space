<template>
  <div class="picker-font">
    <v-menu
      v-model="menu1"
      :close-on-content-click="false"
      transition="scale-transition"
      offset-y
      min-width="auto"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-text-field
          v-model="date"
          prepend-inner-icon="mdi-clock"
          readonly
          dense
          append-icon="mdi-chevron-down"
          height="45"
          background-color="white"
          v-bind="attrs"
          v-on="on"
          outlined
          class="picker-font"
        ></v-text-field>
      </template>
      <v-date-picker v-model="date" @input="menu1 = false"></v-date-picker>
    </v-menu>
    <v-menu
      v-model="menu2"
      :close-on-content-click="false"
      :nudge-right="40"
      transition="scale-transition"
      offset-y
      min-width="auto"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-text-field
          v-model="date"
          prepend-inner-icon="mdi-clock"
          dense
          height="45"
          readonly
          append-icon="mdi-chevron-down"
          background-color="white"
          v-bind="attrs"
          v-on="on"
          outlined
          class="picker-font"
        ></v-text-field>
      </template>
      <v-date-picker v-model="date" @input="menu2 = false"></v-date-picker>
    </v-menu>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      date: new Date(Date.now() - new Date().getTimezoneOffset() * 60000)
        .toISOString()
        .substr(0, 10),
      menu: false,
      modal: false,
      menu1: false,
      menu2: false,
    }
  },
})
</script>