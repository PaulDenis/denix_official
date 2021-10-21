<template>
  <div id="app">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header @active="set_active" />
    <AboutMe v-if="active_page == 1" /> 
    <Projects v-else-if="active_page == 2" />
    <Contacts v-else-if="active_page == 3" />
    <Footer />
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

export default {
  name: 'App',
  components: {
    // HelloWorld
    Header,
    Footer,
    AboutMe,
    Projects,
    Contacts
  },
  data() {
    return {
      active_page: 1
    }
  },
  methods: {
    set_active(active) {
      this.active_page = active;
    }
  }
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
