<template >
    <div>
       <tittlePlus/>
       <boxPlus/>
       <formPlus/>
    </div>
</template>


<script> 
import tittlePlus from '/src/components/compPlus/titlePlus.vue';
import boxPlus from './boxPlus.vue';
import formPlus from './formPlus.vue';
export default {
   components:{
    tittlePlus,
    boxPlus,
    formPlus
   },



    data() {
        return {
            
        }
    },
}
</script>
<style lang="scss" scoped>
    
</style>