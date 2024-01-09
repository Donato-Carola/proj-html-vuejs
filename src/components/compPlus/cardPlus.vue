<template >
    <section class="d-flex container-fluid text-center text-light ">
      <div class="row ">
        
        <div v-for="cards in elementCard" :key="cards.id" class="boxs col-4 pt-5 pb-5" :style="{ backgroundColor: cards.backgroundColor }">
        <h2>{{ cards.title }}</h2>
        <img :src="cards.img" alt="">
        <p>{{ cards.content }}</p>
        <button class="border-light ps-5 pe-5">{{ cards.textButton }}</button>
    </div>
      </div>
      
    </section>
</template>
<script>
export default {
    data() {
        return {
        elementCard: [
        {
          id: 1,
          title: "Emergency Care",
          img:"/public/img/wave-divider.png",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium laudantium,totam rem aperiam,eaque ",
         textButton:"learn more",
         backgroundColor: "#3bafbf"
        },
        {
            id: 2,
          title: "Expert Diagnostics",
          img:"/public/img/wave-divider.png",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium laudantium,totam rem aperiam,eaque ",
         textButton:"learn more",
         backgroundColor: "#3896c2"
        },
        {
            id: 3,
          title: "Superb Rehabilitation",
          img:"/public/img/wave-divider.png",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium laudantium,totam rem aperiam,eaque ",
         textButton:"learn more",
         backgroundColor: "#327ec7"
        }
    ]
        }
    },
}
</script>
<style lang="scss" scoped>
 div.boxs{
    line-height: 2rem;
 }

    button{
        text-transform: uppercase;
        color: white;
        background-color: rgba(0, 0, 0, 0);
        padding: 0.5rem 1rem;
        
        
    }
</style>