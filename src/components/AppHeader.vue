<template >
    <div>
     <h1>{{ info[0].about }}</h1>   
     <h2>{{ info[0].home }}</h2>
    </div>
</template>


<script>
export default {
data() {
    return {
        
    }
},   

props:{
    info:{
        type:Array,
        required:true,
    }
}
}
</script>


<style lang="scss" scoped>

    
</style>