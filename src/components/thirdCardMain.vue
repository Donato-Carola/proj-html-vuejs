<template >
    <section>
        <div>
        <div class="padding">
        <img src="/img/icon-6.png" alt="icona" />
       
        <h1 class="text-uppercase pt-2 pb-2">our health services</h1>
        <div class="w-100 d-flex justify-content-center ">
          <hr class="linea">
         </div>
        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae
          ab illo inventore veritatis et quasi architecto beatae
        </p>
      </div>


        </div>
        <div class="row ">
        <div v-for="specialists in specialist" class="col-lg-4 ">
          <div class="card border-0 align-items-center">
            <img :src="specialists.image" class="card-img-top" alt="..." />
            <div class="card-body text-center">
             
              <h5 class="card-text text-uppercase">
                {{ specialists.title}}
              </h5>
              <p>{{ specialists.content }}</p>
              
            </div>
            
          </div>
        </div>
      </div>
    


        
    </section>
</template>


<script>
export default {
  data() {
    return {
        specialist: [
        {
          id: 1,
          image: "/img/icon-14.png",
          title:"Rehabilitation center",
          content:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          id: 2,
          image: "/img/icon-15.png",
          title:"dental implants",
          content:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          id: 3,
          image: "/img/icon-16.png",
          title:"medicine research",
          content:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          id: 4,
          image: "/img/icon-11.png",
          title:"blood bank",
          content:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          id: 5,
          image: "/img/icon-12.png",
          title:"pharmaceutical advice",
          content:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
          id: 6,
          image: "/img/icon-13.png",
          title:"medical counseling",
          content:
            "At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
      ],
    }
  },    
}
</script>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
div.padding{
   @include centerTitle;
}


h1 {
  color: black;
}

img{
    @include imgSize;
}

hr.linea{
   @include lineSize;
}
</style>
