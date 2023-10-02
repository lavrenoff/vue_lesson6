<template>
  <div id="app">
    <HeaderComponent/>
    <ProjectComponent/>
    <FooterComponent/>
    
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ProjectComponent from './components/ProjectComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    FooterComponent,
    ProjectComponent
  }
}
</script>

<style lang="scss">
@import 'assets/scss/style.scss';

</style>
