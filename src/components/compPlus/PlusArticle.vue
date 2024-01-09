<template >
    <div>
        
       <tittlePlus/>
      
       <cardPlus/>
       <formPlus/>
    </div>
</template>


<script> 
import tittlePlus from '/src/components/compPlus/titlePlus.vue';
import cardPlus from './cardPlus.vue';
import formPlus from './formPlus.vue';
export default {
   components:{
    tittlePlus,
    cardPlus,
    formPlus
   },



    data() {
        return {
            
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../../styles/partials/mixins' as *;


     
</style>