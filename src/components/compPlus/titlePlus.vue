<template >
    <section>
     <article class="title text-light">
        <img src="/img/icon-7.png" alt="">
        <h1 class="text-uppercase pt-2 pb-2">our health services</h1>
        <div class="w-100 d-flex justify-content-center ">
          <hr class="linea">
         </div>
        <p class="ps-5 pe-5 pb-4 pt-2">
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae
          ab illo inventore veritatis et quasi architecto beatae
        </p>

        <img  src="/img/play-icon.png" alt="">
     
     </article>
    </section>
</template>
<script>
export default {
    data() {
        return {
            
        }
    },
}
</script>


<style lang="scss" scoped>

@use "../../styles/partials/mixins" as *;

    section{
        
    background-image: url(/img/paralax-bg-tour-facilities.jpg);
    background-size: cover;
    background-repeat: no-repeat;
     article{
        @include center-content;
        @include centerTitle;
        padding-top: 10rem;
        padding-bottom: 5rem;

       }
    }
     
    img{
        height: 45px;
        width: 45px
    }
  

    hr.linea{
   @include lineSize;
}
</style>