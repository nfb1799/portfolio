<template>
  <v-app>
    <v-app-bar
      id="nav-bar"
      color="black"
    >
      <v-app-bar-title>
        Nik Barbero
      </v-app-bar-title>
      <v-spacer />
      <v-btn  
        style="height: 100%;"
        @click="$router.push({ path: '/' })"
      >
        Home
      </v-btn>
      
      <v-btn  
        style="height: 100%;"
        @click="$router.push({ path: '/gallery' })"
      >
        Gallery
      </v-btn>
      
      <v-btn  
        style="height: 100%;"
        @click="$router.push({ path: '/resume' })"
      >
        Resume
      </v-btn>
      
      <v-btn  
        style="height: 100%;"
        @click="$router.push({ path: '/contact' })"
      >
        Contact
      </v-btn>
    </v-app-bar>
    <RouterView />
  </v-app>

</template>

<script>
import { RouterView } from 'vue-router'
</script>

<style scoped>
</style>
