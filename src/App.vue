<template>
  <div id="app">
    <Header/>
    <Jambotrom/>
    <SectionPopularRecipes/>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Jambotrom from './components/Jambotrom.vue';
import SectionPopularRecipes from './components/SectionPopularRecipes.vue'
export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Jambotrom,
    SectionPopularRecipes
  }
}
</script>

<style lang="scss">
@import '@/style/global.scss';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
