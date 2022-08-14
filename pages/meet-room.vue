<template>
  <div class="d-flex flex-column align-center">
    <v-btn class="btn-positioned text-capitalize body-2 rounded-0 font-weight-bold" elevation="0" to="/coordillera-room">
      See the Coordillera room
    </v-btn>
    <img src="/Layout.png" class="img" />
    <div style="width: 60%" class="d-flex text-left">
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
  width: 80%;  
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
</style>