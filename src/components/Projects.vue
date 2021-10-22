<template>
  <div class="container">
      <h1>My Projects</h1>
      <div class="project_container">
        <div v-for="project in projects" :key="project.title" class="project_card">
            <p><span>Project title:</span> {{ project.title }}</p>
            <p><span>Tecnologyes used:</span> {{ project.tecnology }}</p>
            <p><span>Status of the project:</span> {{ project.state }}</p>
            <a v-if="project.state == 'online'" :href='project.url' target=”_blank”>Link to the project</a>
            <p v-else>No link avalable</p>
        </div>
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
                    title: 'Spotify copy',
                    tecnology: 'HTML, CSS',
                    state: 'online',
                    url: 'https://compassionate-banach-7af1e2.netlify.app/'
                },
                {
                    title: 'Boolzapp (A Whatsapp Web copy)',
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
                },
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    .container {
        height: calc(100vh - 75px);
        border-bottom: 2px solid cyan;
        &>h1 {
            margin-left: 20px;
        }
    }
    .project_container {
        display: flex;
        flex-wrap: wrap;
        justify-content: flex-start;
    }
    .project_card {
        display: flex;
        flex-direction: column;
        width: 30%;
        margin: 20px;
        padding: 20px;
        border-radius: 20px;
        box-shadow: 0 0 3px black;
        background-color: rgb(255, 101, 0);
        & > * {
            align-self: center;
        }
    }
</style>