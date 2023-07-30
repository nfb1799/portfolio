<template>
  <v-app>
    <v-layout>
      <NavBar />
      <v-main>
        <RouterView />
      </v-main>
    </v-layout>
  </v-app>
</template>

<script setup>
import { RouterView } from 'vue-router'
import NavBar from './components/NavBar.vue'
</script>

<style>
#app {
  display: flex;
  margin: 0;
}
</style>
