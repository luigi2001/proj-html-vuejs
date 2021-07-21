<template>
  <div id="app">
    <Header/>
    <Jambotrom/>
    <div class="container">
      <SectionPopularRecipes/>
      <SectionCulinaryCollection/>
      <SectionFarmToTable/>
    </div>
    <Footer/>
  </div>
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';
import Jambotrom from './components/Jambotrom.vue';
import SectionPopularRecipes from './components/SectionPopularRecipes.vue';
import SectionCulinaryCollection from './components/SectionCulinaryCollection.vue';
import SectionFarmToTable from './components/SectionFarmToTable.vue'
export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Jambotrom,
    SectionPopularRecipes,
    SectionCulinaryCollection,
    SectionFarmToTable
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
