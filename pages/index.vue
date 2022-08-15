<template>
  <div>
    <h1 class="font-weight-light text-h3 mt-10">
      <strong class="font-weight-bold"> Find a workspace </strong> that feels
      like home.
    </h1>
    <v-card
      color="#2b63ff"
      elevation="0"
      width="380"
      style="border-radius: 10px"
      class="mt-10 px-6 pb-5"
    >
      <p class="white--text text-h5 pt-10 mb-2 font-weight-medium">
        Start your search
      </p>
      <v-text-field
        outlined
        background-color="white"
        prepend-inner-icon="mdi-map-marker"
        placeholder="NBS ASU"
        dense
        height="45"
      ></v-text-field>
      <menu-picker></menu-picker>
      <v-text-field
        outlined
        dense
        height="45"
        background-color="white"
        prepend-inner-icon="mdi-account"
        placeholder="Who is the reservation for? "
      ></v-text-field>
      <v-text-field
        outlined
        dense
        height="45"
        background-color="white"
        prepend-inner-icon="mdi-account"
        placeholder="For who is it? "
      ></v-text-field>
      <v-checkbox v-model="checkbox" color="white" style="margin-top: -5px">
        <template #label>
          <p class="white--text mb-0">I wanna make a reservation for all day</p>
        </template>
      </v-checkbox>
      <div class="d-flex justify-center mt-5">
        <v-btn
          elevation="0"
          class="font-weight-black grey--text"
          height="45"
          width="100%"
          to="/meet-room"
        >
          Search the workspace
        </v-btn>
      </div>
    <div>
      <div class="circle" />
      <img src="/NestSpace.png" class="img">
    </div>
    </v-card>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import MenuPicker from '~/components/Layout/MenuPicker.vue'
export default Vue.extend({
  components: {
    MenuPicker,
  },
  data(){
    return{
      checkbox: false,
    }
  },
})
</script>

<style scoped>
.title-text{
  font-size: 20px;
  margin-top: 20px;
}
.card-text{
  color: white;
  font-size: 20px;
}
.img {
  position: fixed;
  width: 70%;
  bottom: -280px;
  right: 0;
}
.field-size{
  width: 400px;
  padding-left: 1cm;
}
.circle {
  height: 900px;
  width: 900px;
  position: fixed;
  right: -450px;
  bottom: -200px;
  background: #a8a7a3;
  border-radius: 600px;
}
</style> 