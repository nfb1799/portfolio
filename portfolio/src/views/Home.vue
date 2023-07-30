<template>
  <v-sheet
    id="home-sheet"
    color="black"
    style="height: 100$;"
  >
    <v-row v-if="platform !== 'mobile'">
      <v-col
        cols="5"
        style="display: flex; justify-content: center;"
      >
        <img
          src="../assets/self.png"
        >
      </v-col>
      <v-col
        cols="7"
        style="display: flex; justify-content: center;"  
      >
        <v-card
          id="about-me"
          color="transparent"
        >
          <v-row class="pt-10">
            <v-col
              class="mb-10"  
              cols="12"
            >
              <h1 style="font-weight: bold; font-size: 2.5em;">Web Developer seeking career opportunities</h1>
            </v-col>
            <v-col
              class="pr-10"
              cols="12"
            >
              <h2 style="font-weight: bold;">
                I graduated Summa Cum Laude with a degree in Game Design and Development from Rochester Institute of Technology. 
                I enjoy solving coding puzzles and seeing my ideas come to fruition in the form of web functionality. 
                I have been working as a vue developer since I graduated am always seeking advancement opportunities.
              </h2>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
    <v-row v-else>
      <v-col
        cols="12"
        style="display: flex; justify-content: center;"  
      >
        <v-card
          id="about-me"
          color="transparent"
        >
          <v-row>
            <v-col 
              cols="12"
            >
              <h3 style="font-weight: bold; font-size: 1.5em">Web Developer seeking career opportunities</h3>
            </v-col>
            <v-col
              cols="12"
            >
              <h4 style="font-weight: bold;">
                I graduated Summa Cum Laude with a degree in Game Design and Development from Rochester Institute of Technology. 
                I enjoy solving coding puzzles and seeing my ideas come to fruition in the form of web functionality. 
                I have been working as a vue developer since I graduated am always seeking advancement opportunities.
              </h4>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
      <v-col
        cols="12"
        style="display: flex; justify-content: center;"
      >
        <img
          style="width: 100%;"
          src="../assets/self.png"
        >
      </v-col>
    </v-row>
  </v-sheet>
</template>

<script setup>
import { computed } from 'vue'
import Bowser from 'bowser'

const platform = computed(() => {
  console.log(Bowser.getParser(window.navigator.userAgent).getPlatformType())
  return Bowser.getParser(window.navigator.userAgent).getPlatformType()
})
</script>

<style>
#home-sheet {
  height: 100%;
  background: url('../assets/stars.jpg');
  background-size: cover;
}
</style>
