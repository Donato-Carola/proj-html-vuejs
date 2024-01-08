<template >
    <div>
     <img :src=" info[0].logo " alt="logo">
     <h1>{{ info[0].about }}</h1>   
     <h2>{{ info[0].home }}</h2>
     
    </div>
</template>


<script>
export default {
props:{
    info:{
        type:Array,
        required:true
    }
},


    data() {
    return {
        
    }
},   


}
</script>


<style lang="scss" scoped>

    
</style>