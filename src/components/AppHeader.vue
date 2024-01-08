<template >
<header>
    <section class=" container d-flex justify-content-between w-100 ">
        <div> 
            <img :src=" info[0].logo " alt="logo">
        </div>
    
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
    background-image: url(../assets/img/header-image-homepage.jpg);
    object-fit: cover;
    height:500px;
}
ul{
    list-style: none;
    display: flex;
    
    
}
    
</style>