<template >
<header>
    <img src="/public/img/header-image-homepage.jpg" alt="">
    <section class=" container d-flex justify-content-between align-items-center pt-2">
       
            <img class="w-25" :src=" info[0].logo " alt="logo">
       
    
    <ul class="text-center">
        <li>
           {{ info[0].home }}
        </li>
        <li>
            {{ info[0].about }}
        </li>
        <li>
            {{ info[0].departments}}
        </li>
        <li>
            {{ info[0].articles }}
        </li>
        <li>
            {{ info[0].appointment}}
        </li>
    </ul>
     
    </section>
</header>
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

header{
    position: relative;
}

section{
    height: 100px;

}

ul{
    list-style: none;
    display: flex;
    li{
        padding-left: 1rem;
    }
    
}
    
</style>