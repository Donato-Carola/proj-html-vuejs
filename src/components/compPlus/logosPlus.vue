<template lang="">
  <div>
    <section class="iconss">
      <article>
        <div>
        <img src="/img/client-logos-1.png" alt="" />
        <img src="/img/client-logos-2.png" alt="" />
        <img src="/img/client-logos-3.png" alt="" />
        <img src="/img/client-logos-4.png" alt="" />
     </div>
      </article>
    </section>
  </div>
</template>


<script>
export default {
    data() {
        return {
            
        }
    },
};
</script>
<style lang="scss" scoped>
@use "../../styles/partials/mixins" as *;

section.iconss{
     background-image: radial-gradient(circle at left center, #3bafbf, #3896c2);
}

article{

position: relative;
  width: 1100px;
  margin: 0 auto;
  height: 300px; // O regola l'altezza in base alle tue esigenze
  overflow: hidden;

 
  
  
  
  div{
  position: absolute;
  top: 0;
  left:50%;
  width: 50%;
  height: 100%;
  display: flex;
  align-items: center;
  animation: slideRight 8s infinite linear; 
 
  
  }
}

div img {
  flex: 0 0 25%; // Larghezza di ogni icona, occupa un quarto dello spazio
  height: auto; // Occupa tutta l'altezza della section
  opacity: 0;
  animation:fadeInOut 12s infinite linear;
  
}

@keyframes slideRight {
  0% {
    transform: translateX(0%);
  }
  100%{
    transform: translateX(-100%);
  }


}

@keyframes fadeInOut{
    0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 1;
  }
}
</style>
