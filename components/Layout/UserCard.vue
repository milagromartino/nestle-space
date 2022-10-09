<template>
  <v-select
    v-model="selectedUser"
    :items="users"
    item-text="name"
    item-value="id"
    solo
    flat
    filled
    style="width: 250px"
    background-color="#f3f0e9"
    class="mt-7 elevation-0 rounded-0 font-weight-medium"
  >
    <template #prepend-inner>
      <v-img :src="selectedUserProfile" width="40" contain></v-img> </template
    >/>
  </v-select>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
  data() {
    return {
      selectedUserProfile: '/profile-pic.png',
      selectedUser: 'Rodrigo Orella',
      users: [
        {
          name: 'Rodrigo Orella',
          icon: '/profile-pic.png',
        },
        {
          name: 'Carlota Carlota',
          icon: '/profile-pic.png',
        },
      ],
    }
  },
})
</script>