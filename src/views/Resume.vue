<template>
  <div style="background-color: #d4d4d4; height: 100%; display: flex; justify-content: center;">
    <iframe
      :src="resume"
      width="95%"
      height="100%"  
    />
  </div>
</template>

<script>
import Resume from '../assets/ResumeNikBarbero.pdf'
export default {
  data () {
    return {
      resume: Resume,
    }
  }
}
</script>

<style>

</style>