<template>
  <div class="container">
      <h1>My Projects</h1>
      <div v-for="project in projects" :key="project.title">
        <p>{{ project.title }}</p>
        <p>{{ project.tecnology }}</p>
        <p>{{ project.state }}</p>
        <a v-if="project.state == 'online'" :href='project.url' target=”_blank”>Link to the project</a>

      </div>
  </div>
</template>

<script>
export default {
    name:'Projects',
    data() {
        return {
            projects: [
                {
                    title: 'Spotify',
                    tecnology: 'HTML, CSS',
                    state: 'online',
                    url: 'https://compassionate-banach-7af1e2.netlify.app/'
                },
                {
                    title: 'Whatsapp Web',
                    tecnology: 'HTML, CSS, JAVASCRIPT',
                    state: 'online',
                    url: 'https://gallant-kepler-cefe7e.netlify.app/'
                },
                {
                    title: 'Digital Ocean copy',
                    tecnology: 'HTML, CSS',
                    state: 'online',
                    url: 'https://keen-roentgen-0e3540.netlify.app/'
                },
                {
                    title: 'Boolflix (A netflix copy)',
                    tecnology: 'HTML, CSS, JAVASCRIPT, VUE',
                    state: 'offline',
                    url: ''
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .container {
        height: calc(100vh - 75px);
        border-bottom: 2px solid cyan;
    }
</style>