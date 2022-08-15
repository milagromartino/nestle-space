<template>
  <v-app>
    <app-bar></app-bar>
    <v-main class="set-color px-16">
      <v-container >
        <Nuxt />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import AppBar from '~/components/Layout/AppBar.vue'
export default {
  components: { AppBar },
  data: () => ({
  })
}
</script>

<style>
.set-color{
  background-color: #f3f0e9;
}
</style>