<template>
  <div class="picker-font">
    <!-- first menu picker. (date picker) -->
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
          prepend-inner-icon="mdi-calendar-month-outline"
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
    <!-- second menu picker. (time picker) -->
    <v-menu
      ref="menu"
      v-model="menu2"
      :close-on-content-click="false"
      :nudge-right="40"
      :return-value.sync="time"
      transition="scale-transition"
      offset-y
      max-width="290px"
      min-width="290px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-text-field
          v-model="time"
          prepend-inner-icon="mdi-clock-time-four-outline"
          readonly
          label="Pick a time"
          dense
          append-icon="mdi-chevron-down"
          height="45"
          background-color="white"
          v-bind="attrs"
          v-on="on"
          outlined
        ></v-text-field>
      </template>
      <v-time-picker
        v-if="menu2"
        v-model="time"
        full-width
        @click:minute="$refs.menu.save(time)"
      ></v-time-picker>
    </v-menu>
    <v-dialog
      ref="dialog"
      v-model="modal2"
      :return-value.sync="time"
      width="290px"
    >
      <template v-slot:activator="{ on, attrs }">
        <v-text-field
          v-model="time2"
          prepend-inner-icon="mdi-clock-time-four-outline"
          readonly
          dense
          label="Pick a time"
          append-icon="mdi-chevron-down"
          height="45"
          background-color="white"
          v-bind="attrs"
          v-on="on"
          outlined
        ></v-text-field>
      </template>
      <v-time-picker v-if="modal2" v-model="time2" full-width>
        <v-spacer></v-spacer>
        <v-btn text color="primary" @click="modal2 = false"> Cancelar </v-btn>
        <v-btn text color="primary" @click="$refs.dialog.save(time)">
          OK
        </v-btn>
      </v-time-picker>
    </v-dialog>
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
      time: null,
      time2: null,
      menu: false,
      modal: false,
      modal2: false,
      menu1: false,
      menu2: false,
    }
  },
})
</script> 