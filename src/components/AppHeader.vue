<template>
  <header>
    <section 
      class=" topSection container d-flex justify-content-between align-items-center pt-4 "
    >
      <img class="w-25" :src="info[0].logo" alt="logo" />

      <ul class="text-uppercase firstul">
        <li class="arrow firstli" v-for="infotwo in infoTwo"
        @mouseover="showDropdown[infotwo.home] = true"
       >
        
      <div class="d-flex align-content-center align-items-center ">
          {{ infotwo.home }} <i class="fa-solid fa-chevron-down arrow ps-1"></i>
        </div>
          <ul  v-if="showDropdown[infotwo.home]" class="dropdown ulGhost ">
             <li class="liGhost" v-for="content in dropdownContents[infotwo.home]" @click="closeDropdown(infotwo.home)">
         <a href="#">{{ content }} </a> 
             </li>
          </ul>
        </li>
     
        <li class="firstli">
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
    infoTwo:{
      type:Array,
      required:true,
      
    }
  },


  data() {
    return {
      showDropdown: {},
      dropdownContents:{
        'Home': ['Contenuto 1A', 'Contenuto 1B'],
        'About': ['Contenuto 2A', 'Contenuto 2B'],
        'Departments': ['General Practice', 'Cardiology', 'Pediatrics', 'Diabetes Care', 'Pre-natal Care', 'Ultrasound Echocardiogram'],
        'Articles': ['Contenuto 4A', 'Contenuto 4B']
    }
    };
  },

  methods: {
  toggleDropdown(home) {
    this.showDropdown[home] = !this.showDropdown[home];
  },
  closeDropdown(home) {
    this.showDropdown[home] = false;
  }
}

};
</script>

<style lang="scss" scoped>
header {
  background-image: url(/img/header-image-homepage.jpg);
  background-size: cover;
  background-repeat: no-repeat;
}

section.topSection {
 padding-bottom: 15rem;
  img {
    object-fit: cover;
  }
}

ul.firstul {
  color: white;
  list-style: none;
  display: flex;
  align-items: center;
 
} 
li.firstli:hover{
  color:#327ec7
}
i.arrow{
  display: none;
}
li.firstli:hover i.arrow{
  display: block;
}

li.firstli {
    padding-left: 1rem;
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

    button:hover{
      background-color: #327ec7;
    }

    .dropdown {
  position: absolute;
  
  color: black;
  background-color: #fff; /* Sfondo bianco per il menu */
  list-style: none;
  z-index:9999; /* Assicura che il menu a tendina sia sopra gli altri elementi */
  display: none; /* Inizialmente nascosto */
  line-height: 5rem;
  padding: 0 0.5rem 0 0.5rem;
  
}

.arrow:hover .dropdown {
  display:block; /* Mostra il menu a tendina quando si passa con il mouse sopra l'elemento con classe arrow */
}

a{
 text-decoration: none;
 color: black;
}
    
   
</style>
