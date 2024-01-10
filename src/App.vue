<template>
 <AppHeader :info="infoHeader" :infoTwo="infoHeaderTwo" />
 <AppMain/>

 <AppFooter :infoFooter="infoFooter"/>
</template>



<script >
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

import data from './data/dataHeader.json'
import dataTwo from './data/dataHeaderTwo.json'

export default{
  components: {
        AppHeader,
        AppMain,
        AppFooter
  },



  data() {
    return {
      infoHeader:data.header,
      infoFooter:data.footer,
      infoHeaderTwo:dataTwo.headertwo
    };
  },

 

 
}




</script>



<style lang="scss" >
@use "./styles/general.scss"
</style>
