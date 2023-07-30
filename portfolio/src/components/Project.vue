<template>
  <div>
    <v-row>
      <v-col cols="6">
        <img
          :src="imageSrc"
          style="width: 100%;"
        >
      </v-col>
      <v-col cols="6">
        <v-row>
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
  }
}
</script>

<style>

</style>