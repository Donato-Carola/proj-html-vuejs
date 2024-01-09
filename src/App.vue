<template>
 <AppHeader :info="infoHeader" />
 <AppMain/>

 <AppFooter :infoFooter="infoFooter"/>
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
      infoHeader:data.header,
      infoFooter:data.footer
    };
  },

 

 
}




</script>



<style lang="scss" >
@use "./styles/general.scss"
</style>
