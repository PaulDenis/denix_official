<template>
  <div id="app">
    <div v-if="isLoading" class="loader"> <!-- Create a real Loader -->
      <img src="./assets/th.gif" alt="Loading" id="loader"> 
      <img src="./assets/logo.png" alt="Fox logo" class="loading_logo">
    </div>
    <div v-else>
      <div v-if="active_page == 0" class="container">
        <Landing @active="set_active"/>
      </div>
      <div v-else>
        <Header @active="set_active" />
        <AboutMe v-if="active_page == 1" /> 
        <Projects v-else-if="active_page == 2" />
        <Contacts v-else-if="active_page == 3" />
        <Footer />
      </div>
    </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
// import Content from './components/Content.vue'
import AboutMe from './components/About_me.vue'
import Projects from './components/Projects.vue'
import Contacts from './components/Contacts.vue'
import Landing from './components/Landing.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header,
    Footer,
    AboutMe,
    Projects,
    Contacts,
    Landing
  },
  data() {
    return {
      active_page: 0,
      isLoading: true
    }
  },
  methods: {
    set_active(active) {
      this.active_page = active;
    },
    stopLoading() {
      setTimeout(() =>  {
        this.isLoading = false;
      }, 1000);
    }
  },
  mounted() {
    this.stopLoading();
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#loader {
  height: 50vh;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 1;
}
.loading_logo {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  height: 50vh;
  z-index: 2;
}

</style>
