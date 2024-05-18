<template>
  <div id="app">
    <HeaderPage />
    <BunnerComponent />
    <ProjectsComponent />
    <FooterPage />
  </div>
</template>

<script>
import FooterPage from './../../final-examination/src/components/FooterPage.vue'
import HeaderPage from './../../final-examination/src/components/HeaderPage.vue'
import BunnerComponent from './components/BunnerComponent.vue'
import ProjectsComponent from './components/ProjectsComponent.vue'

export default {
  name: 'App',
  components: {
    FooterPage,
    HeaderPage,
    BunnerComponent,
    ProjectsComponent
  }
}
</script>

<style>
#app {
    
}
a{
  text-decoration: none;
}
</style>
