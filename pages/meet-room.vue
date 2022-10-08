<template>
  <div class="d-flex flex-column align-center">
    <v-btn
      class="btn-positioned text-capitalize body-2 rounded-0 font-weight-bold"
      elevation="0"
      to="/coordillera-room"
    >
      See the Coordillera room
    </v-btn>
    <img src="/Layout.png" class="img" />
    <div style="width: 60%" class="d-flex text-left">
      <div class="button-1">
        <v-row align="center">
          <div class="pl-4">
          <v-btn fab block color="#006ffa" x-small elevation="0" > <h2 class="font-weight-bold white--text">8</h2></v-btn>
          </div>
          <div class="pl-4">
          <v-btn fab block color="#f16463" x-small elevation="0" > <h2 class="font-weight-bold white--text">7</h2></v-btn>
          </div>
          <div class="pl-4">
          <v-btn fab block color="#f16463" x-small elevation="0" > <h2 class="font-weight-bold white--text">6</h2></v-btn>
          </div>
          <div class="pl-3">
          <v-btn fab block color="#f16463" x-small elevation="0" > <h2 class="font-weight-bold white--text">5</h2></v-btn>
          </div>
        </v-row>
         <v-row align="center" class="mt-9">
          <div class="pl-4">
          <v-btn fab block color="#f16463" x-small elevation="0" > <h2 class="font-weight-bold white--text">4</h2></v-btn>
          </div>
          <div class="pl-4">
          <v-btn fab block color="#f16463" x-small elevation="0" > <h2 class="font-weight-bold white--text">3</h2></v-btn>
          </div>
          <div class="pl-4">
          <v-btn fab block color="#f16463" x-small elevation="0" > <h2 class="font-weight-bold white--text">2</h2></v-btn>
          </div>
          <div class="pl-3">
          <v-btn fab block color="#006ffa" x-small elevation="0" > <h2 class="font-weight-bold white--text">1</h2></v-btn>
          </div>
        </v-row>
      </div>
      <p class="font-weight-medium">Superscription</p>
      <div class="circle-blue mx-3"></div>
      <p class="font-weight-light">Available</p>
      <div class="circle-red mx-3"></div>
      <p class="font-weight-light">Busy</p>
    </div>
  </div>
</template>

<style scoped>
.img {
  width: 90%;
  position:static ;
}
.circle-red {
  border-radius: 30px;
  width: 25px;
  height: 25px;
  background: #f16463;
}
.circle-blue {
  border-radius: 30px;
  width: 25px;
  height: 25px;
  background: #006ffa;
}
.btn-positioned {
  color: #3563a9;
  background: #ffd382 !important;
  position: absolute;
  right: 120px;
  top: 20px;
}
.button-1 {
position: absolute;
bottom:4em;
top: 19cm;
border-radius:4em;
padding:20px 20px;
justify-content: space-around;
}
</style> 