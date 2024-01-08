<template>
 <AppHeader :info="infoHeader" />
 <AppMain/>

 <AppFooter/>
</template>



<script >
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

import data from './data/dataHeader.json'

export default{
  components: {
        AppHeader,
        AppMain,
        AppFooter
  },



  data() {
    return {
      infoHeader:data.header
    };
  },

 

 
}




</script>



<style lang="scss" >
@use "./styles/general.scss"
</style>
