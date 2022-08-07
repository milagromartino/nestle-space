<template>
  <div>
    <div class="title-text">
      <h1> <strong> Find a workspace </strong> that feels like home.</h1>
    </div>
    <v-card color="#2b63ff" elevation="0" rounded="4" width="450"  height="650" class="mt-8">
      <v-card-title class="card-text pl-10">Start your search</v-card-title>
       <div class="field-size">
        <v-text-field outlined background-color="white" prepend-inner-icon="mdi-map-marker" placeholder="NBS ASU"></v-text-field>
      </div>
     <menu-picker></menu-picker>
     <div class="field-size">
        <v-text-field outlined background-color="white" prepend-inner-icon="mdi-account" placeholder="Who is the reservation for? "></v-text-field>
        <v-text-field outlined background-color="white" prepend-inner-icon="mdi-account" placeholder="For who is it? "></v-text-field>
      </div>
      <v-checkbox v-model="checkbox" class="pl-10" color="white">
      <template v-slot:label class="checkbox-color">
        <div class="white--text"> 
          I wanna make
          a reservation
          for all day
        </div>
      </template>
    </v-checkbox>
    <div class="d-flex justify-center">
     <v-btn elevation="0" class="d-flex" width="360">
      Search the workspace
    </v-btn>  
    </div>
   
    </v-card>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import MenuPicker from '~/components/Layout/MenuPicker.vue'
export default Vue.extend({
  data(){
    return{
      checkbox: false,
    }
  },
  components:{
    MenuPicker,
  }
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
.field-size{
  width: 400px;
  padding-left: 1cm;
}
.checkbox-color{
  color: white;
}

</style>