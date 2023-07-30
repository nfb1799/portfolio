<template>
  <div>
    <v-row>
      <v-col
        :class="platform === 'mobile' ? 'pb-0' : ''"
        :cols="platform === 'mobile' ? 12 : 5"  
      >
        <img
          :src="imageSrc"
          style="width: 100%;"
        >
      </v-col>
      <v-col
        :class="platform === 'mobile' ? 'pt-0 mb-8' : 'pr-8'"
        :cols="platform === 'mobile' ? 12 : 7"  
      >
        <v-row class="mb-4">
          <a :href="link">
            <h1>
              {{ title }}
            </h1>
          </a>
        </v-row>
        <v-row>
          <h3><b>Description: </b>{{ description }}</h3>
        </v-row>
        <v-row>
          <h3><b>Technologies Used: </b>{{ technologies }}</h3>
        </v-row>
        <v-row>
          <h3><b>Roles: </b>{{ roles }}</h3>
        </v-row>
        <v-row>
          <h3><b>Learning Outcomes: </b>{{ learningOutcomes }}</h3>
        </v-row>
        <v-row>
          <h3><b>Challenges: </b>{{ challenges }}</h3>
        </v-row>
      </v-col>
    </v-row>
  </div>
</template>

<script>
import Bowser from 'bowser'
export default {
  name: 'Project',
  props: {
    title: String,
    link: String,
    imageSrc: String,
    description: String,
    technologies: String,
    roles: String,
    learningOutcomes: String,
    challenges: String,
  },
  computed: {
    platform () {
      return Bowser.getParser(window.navigator.userAgent).getPlatformType()
    },
  }
}
</script>

<style>

</style>