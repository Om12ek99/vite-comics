<script >
import AppHeader from './components/AppHeader.vue';
import AppIcons from './components/AppIcons.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

  export default {         //aggiungo
    components: {
      AppHeader,
      AppMain,
      AppIcons,
      AppFooter
    }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
  <AppIcons/>
  <AppFooter/>
</template>

<style lang = "scss">    //aggiungo 
  


</style>
