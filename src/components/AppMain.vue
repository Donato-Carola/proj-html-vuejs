<template>
  <main>
    <section>



      <article class="firstArticle">
        <div class="titleArticle">
        <h1>Welcome to Avada Health</h1>
        <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo</p>
      </div>
     <div class="row">
         <firstCardMain v-for="card in cards" 
         :key=card.id
         :card="card"
         />
        </div>   
        
      </article>





    </section>
  </main>
</template>

<script>

import firstCardMain from './firstCardMain.vue';


export default {
components:{
    firstCardMain
},
  data() {
    return {
     


        cards: [
        { id: 1, title: "same day appointments", content: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ", image: "/img/icon-1.png" },
        { id: 2, title: "world class facilities", content: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ", image: "/img/icon-2.png" },
        { id: 3, title: "expert doctors", content: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ", image: "/img/icon-3.png" },
        { id: 4, title: "complementary therapies", content: "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ", image: "/img/icon-4.png" }
      ]

        
    };
  },
};
</script>

<style lang="scss" scoped>
@use '../styles/partials/mixins' as *;
section{
   @include center-content;
  padding-top: 5rem;

}
div.titleArticle{
    padding: 0 8rem;
}


</style>
