<template>
  <a :href="link" target="_blank" rel="noopener" style="text-decoration: none; color: inherit;">
<v-card class="project-card" elevation="4" hover>
      <v-card-title class="project-title">
        <h2 class="pb-2">{{ title }}</h2>
      </v-card-title>
      <v-img :src="imageSrc" height="200px" cover></v-img>
      <v-card-text class="project-card-text">
        <div class="project-card-content">
          <div><b>Description:</b> {{ description }}</div>
          <div><b>Technologies Used:</b> {{ technologies }}</div>
          <div><b>Roles:</b> {{ roles }}</div>
          <div><b>Learning Outcomes:</b> {{ learningOutcomes }}</div>
          <div><b>Challenges:</b> {{ challenges }}</div>
        </div>
      </v-card-text>
    </v-card>
  </a>
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
  },
}
</script>

<style scoped>
.project-card {
  min-height: 480px;
  max-height: 520px;
  height: 100%;
  margin: 8px auto;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  transition: box-shadow 0.2s, transform 0.2s;
  cursor: pointer;
}
.project-card:hover {
  box-shadow: 0 8px 24px rgba(0,0,0,0.18), 0 1.5px 6px rgba(0,0,0,0.12);
  transform: translateY(-4px) scale(1.03);
  background-color: #f5f5f5;
}
.project-title {
  padding-bottom: 0;
}
.project-card-text {
  font-size: 0.98rem;
  padding-top: 8px;
  padding-bottom: 12px;
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  justify-content: stretch;
  height: 100%;
}
.project-card-content {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
}
</style>