<template>
  <header>
    <section 
      class=" topSection container d-flex justify-content-between align-items-center pt-4 "
    >
      <img class="w-25" :src="info[0].logo" alt="logo" />

      <ul >
        <li>
          {{ info[0].home }}
        </li>
        <li>
          {{ info[0].about }}
        </li>
        <li>
          {{ info[0].departments }}
        </li>
        <li>
          {{ info[0].articles }}
        </li>
        <li >
            <button  class="border-0 ">{{ info[0].appointment }}</button>
          
        </li>
      </ul>
    </section>
          
    <section class="more">
       <h1 class="pb-2">
        <span>Caring</span>
         For Life</h1>
       <p class="pb-2 text-light">{{ info[0].text }}</p>
       <button  type="button" class="border-0 ">learn more</button>
        


    </section>
  </header>
</template>

<script>
export default {
  props: {
    info: {
      type: Array,
      required: true,
    },
  },

  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
header {
  background-image: url(/img/header-image-homepage.jpg);
  object-fit: cover;
  background-repeat: no-repeat;
}

section.topSection {
 padding-bottom: 15rem;
  img {
    object-fit: cover;
  }
}

ul {
    color: white;
  list-style: none;
  display: flex;
  align-items: center;
  li {
    padding-left: 1rem;
  }
}

section.more{
    width: 850px;
    margin: 0 auto;
    padding-bottom:20rem;
    h1{
        color: #3bafbf;
        span{
            color: white;
        }
    }
   
    } button{
        text-transform: uppercase;
        color: white;
        background-color: #3bafbf;
        padding: 0.5rem 1rem;
        
    }
</style>
