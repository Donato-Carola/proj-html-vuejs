<template>
  <section>
    <div class="row container-fluid">
      <article
        v-for="infos in infoFooter"
        :key="infos.id"
        class="d-flex justify-content-between p-4"
      >
        <div class="pe-4 col-4">
          <img :src="infos.logo" alt="" />
          <p>{{ infos.text }}</p>
          <div class="w-100 d-flex justify-content-center">
            <hr class="linea" />
          </div>
          <h5>{{ infos.info }}</h5>
          
          <i class="fab fa-facebook pe-1"></i>
          <i class="fab fa-twitter pe-1"></i>
          <i class="fab fa-instagram"></i>
        </div>

        <div class="pe-4 col-4">
         <h5 class="text-uppercase">Contact information</h5>
         <div class="linea"></div>
          <h5>{{ infos.contact.position }}</h5>
          <h5>{{ infos.contact.tell }}</h5>
       </div>


        

        <div class="pe-4 col-4">
            <h5 class="text-uppercase">{{ infos.medical }}</h5>
            <div class="linea"></div>
            <ul class="p-0">
                <li>{{ infos.specialist }}</li>
                <li>{{ infos.specialist1 }}</li>
                <li>{{ infos.specialist2 }}</li>
                <li>{{ infos.specialist3 }}</li>
                <li>{{ infos.specialist4 }}</li>

            </ul>
            <button class="text-uppercase">View our departments</button>
            </div>
      </article>
    </div>
  </section>
</template>
<script>
export default {
  props: {
    infoFooter: {
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
@use "../../src/styles/partials/mixins" as *;
hr.linea {
  width: 100%;
}

div.linea{
    border: 1px solid #3bafbf;
    width: 30px;
}

ul{
    list-style: none;
}

button{
    border: 0.5px solid black;
    background-color: rgba(0, 0, 0, 0);
    padding: 1rem 2rem;

}
</style>
