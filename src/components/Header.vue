<template>
  <div class="main-container">
      <nav class="navbar navbar-expand-lg navbar-light bg-light">
  <div class="container-fluid">
    <a class="navbar-brand" href="#" @click="active_page = 1, $emit('active', active_page)">
      <img src="../assets/logo.png" alt="Fox logo" id="logo">
    </a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNavAltMarkup" aria-controls="navbarNavAltMarkup" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNavAltMarkup">
      <div class="navbar-nav">
        <a class="nav-link" 
        :class="[active_page == 1 ? 'active' : '']"  
        href="#" 
        @click="active_page=1, $emit('active', active_page)">About me</a>
        <a class="nav-link" 
        :class="[active_page == 2 ? 'active' : '']" 
        href="#" 
        @click="active_page=2, $emit('active', active_page)">My projects</a>
        <a class="nav-link" 
        :class="[active_page == 3 ? 'active' : '']" 
        href="#" 
        @click="active_page=3, $emit('active', active_page)">Contacts</a>
        <!-- <a class="nav-link disabled">Disabled</a> -->
      </div>
    </div>
  </div>
</nav>
  </div>
</template>

<script>
export default {
    name: 'Header',
    data() {
      return {
        active_page: 1
      }
    },
}
</script>

<style lang="scss" scoped>
@import 'bootstrap';


.main-container {
    height: 75px;
    border-bottom: 2px solid cyan;
}
#logo {
  height: 75px;
  margin: -15px;
}

</style>