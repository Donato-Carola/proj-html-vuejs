<template>
  <section>
    <article class="title text-light">
      <h1 class="text-uppercase pt-2 pb-2">Make An Appointment</h1>
      <div class="w-100 d-flex justify-content-center">
        <hr class="linea" />
      </div>
      <p class="ps-5 pe-5 pb-4 pt-2">
        Sed ut perspiciatis unde omnis iste natus error sit voluptatem
        accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab
        illo inventore veritatis et quasi architecto beatae
      </p>

      <div class="row ">
        <div class="col-6">
          <div class="mb-3" >
           
            <input
              type="text"
              class="w-100 bg-transparent text-light"
              id="exampleFormControlInput1"
              placeholder="Name*"
            />
          </div>
        </div>
        <div class="col-6">
          <div class="mb-3">
          
            <input
              type="text"
              class="w-100 bg-transparent text-light"
              id="exampleFormControlInput1"
              placeholder="Email*"
            />
          </div>
        </div>
        <div class="col-6">
          <div class="mb-3">
           
            <input
              type="text"
              class="w-100 bg-transparent text-light"
              id="exampleFormControlInput1"
              placeholder="Phone Number"
            />
          </div>
        </div>
        <div class="col-6">
          <div class="mb-3">
           
            <input
              type="text"
              class="w-100 bg-transparent text-light"
              id="exampleFormControlInput1"
              placeholder=" Appointment Date"
            />
          </div>
        </div>
        <div class="col-12">
          <div class="mb-3">
           
            <textarea
            class="w-100 bg-transparent text-light"
              id="exampleFormControlTextarea1"
              rows="3"
              placeholder="How can we help?*"
            ></textarea>
          </div>
        </div>
        <button class=" border-0  text-light ">MAKE AN APPOINTMENT</button>
      </div>
    </article>
  </section>
</template>
<script>
export default {
  data() {
    return {};
  },
};
</script>
<style lang="scss" scoped>
@use "../../styles/partials/mixins" as *;

section {
  background-image: url(/img/make-an-appointment.jpg);
  background-size: cover;
  background-repeat: no-repeat;
  article {
    @include center-content;
    @include centerTitle;
    padding-top: 10rem;
    padding-bottom: 5rem;
  }
}
hr.linea {
  @include lineSize;
}

button{
        text-transform: uppercase;
        color: white;
        background-color: #3bafbf;
        padding: 0.5rem 1rem;
        width: calc(100% - 1rem);
        margin-left: 0.5rem;
        
    }
    input,
    textarea{
        padding: 1rem 1.5rem;
        border: 0.5px solid white;
    }
</style>
