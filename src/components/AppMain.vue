<template>
  <main>
    <section>
      <article class="firstArticle">
        <div class="ridimensiona">
          <div class="titleArticle">
            <h1>Welcome to Avada Health</h1>
            <p>
              Sed ut perspiciatis unde omnis iste natus error sit voluptatem
              accusantium doloremque laudantium, totam rem aperiam, eaque ipsa
              quae ab illo
            </p>
          </div>
          <div class="row">
            <firstCardMain v-for="card in cards" :key="card.id" :card="card" />
          </div>
        </div>
      </article>

      <article class="secondArticle">
        <div class="ridimensiona">
          <secondCardMain />
        </div>
      </article>

      <article class="thirdArticle">
        <div class="ridimensiona"></div>   
     <thirdCardMain/>
      </article>


    </section>
  </main>
</template>

<script>
import firstCardMain from "./firstCardMain.vue";
import secondCardMain from "./secondCardMain.vue";
import thirdCardMain from "./thirdCardMain.vue";

export default {
  components: {
    firstCardMain,
    secondCardMain,
    thirdCardMain
  },
  data() {
    return {
      cards: [
        {
          id: 1,
          title: "same day appointments",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ",
          image: "/img/icon-1.png",
        },
        {
          id: 2,
          title: "world class facilities",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ",
          image: "/img/icon-2.png",
        },
        {
          id: 3,
          title: "expert doctors",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ",
          image: "/img/icon-3.png",
        },
        {
          id: 4,
          title: "complementary therapies",
          content:
            "Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium ",
          image: "/img/icon-4.png",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
@use "../styles/partials/mixins" as *;
section {
  padding-top: 5rem;
}
div.ridimensiona {
  @include center-content;
  padding-bottom: 5rem;
}
div.titleArticle {
   @include centerTitle;

}

article.secondArticle {
  background-color: #e5e5e5;
}
</style>
