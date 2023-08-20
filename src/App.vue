<script>
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
export default{
  name:'App',
  components:{
    AppFooter,
    AppMain
  }
}
</script>

<template>
  <AppMain/>
  <AppFooter/>
    
</template>

<style lang="scss">
    @import './styles/general.scss';
</style>
