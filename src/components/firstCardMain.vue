<template >
   
  <div class="first card border-0 col-lg-3 flex-nowrap d-flex align-items-center" >
  <img :src="card.image" class="" alt="...">
  <div class="card-body">
    <h5 class="card-title">{{card.title}}</h5>
    <p class="card-text">{{card.content}}</p>
    
  </div>
</div>

</template>
<script>
export default {
    props:{
        card:{
            type:Object,
            required:true
        }
    }
    
}
</script>
<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
img{
   @include imgSize;
  }

 div.first:hover h5{
    color: #3bafbf;
  }

</style>