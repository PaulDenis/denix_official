<template>
  <div id="app">
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
      active_page: 0
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
