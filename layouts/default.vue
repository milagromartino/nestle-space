<template>
  <v-app>
    <app-bar></app-bar>
    <v-main >
      <v-container>
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
</style>