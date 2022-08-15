<template>
  <v-app-bar class="px-15" app elevation="0" color="#f3f0e9">
    <div class="d-flex align-center">
      <v-img src="/nestle-logo.png" width="120" contain class="img-filter" @click="$router.push('/')" />
      <p class="mb-0 text-h6 ml-3">NestSpace</p>
    </div>
    <v-spacer></v-spacer>
    <div class="d-flex align-center">
      <user-card></user-card>
      <div class="d-flex align-center">
        <v-icon>mdi-account-outline</v-icon>
        <span class="ml-3">Private Area</span>
      </div>
    </div>
  </v-app-bar>
</template>

<script lang="ts">
import Vue from 'vue'
import UserCard from '~/components/Layout/UserCard.vue'
export default Vue.extend({
  components: { UserCard },
})
</script>

<style scoped>
.img-filter {
  filter: brightness(0.26) saturate(0.07);
}
</style>