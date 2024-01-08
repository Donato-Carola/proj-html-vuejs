<template>
 <AppHeader :info="infoHeader"/>
 <AppMain/>

 <AppFooter/>
</template>



<script >
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import axios from 'axios';

export default{
  components: {
        AppHeader,
        AppMain,
        AppFooter
  },



  data() {
    return {
      infoHeader:[{}]
    }
  },

 

  methods: {
    fetchData() {
      axios.get('../src/data/dataHeader.json')  
        .then((response)=>{
          console.log(response.data);
          this.infoHeader = response.data;
          
        })
        .catch(error => {
          console.error('Errore nel caricamento dei dati:', error);
        });
    }
  },

   created() {
    this.fetchData();
  },
}




</script>



<style lang="scss" >
@use "./styles/general.scss"
</style>
