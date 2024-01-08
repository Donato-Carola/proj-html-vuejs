<template>
  <section>
    <div>
      <div class="text-center">
        <img src="/img/icon-5.png" alt="icona" />
        <h1 class="text-uppercase">meet our doctors</h1>

        <p>
          Sed ut perspiciatis unde omnis iste natus error sit voluptatem
          accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae
          ab illo inventore veritatis et quasi architecto beatae
        </p>
      </div> 
      <div class="row">
      <div v-for="doctors in doctor" class="col-lg-4">
      
        <div class="card ">
          <img :src="doctors.image" class="card-img-top" alt="..." />
          <div class="card-body">
            <h5 class="card-title">{{doctors.name}}</h5>
            <h5 class="card-text">
             {{doctors.specialist}}
            </h5>
            <p>{{ doctors.content }}</p>
          </div>
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
      doctor: [
        {
          id: 1,
          name: "jon snow",

          specialist: "Anesthesiologist ",
          image: "/img/doctor-1.jpg",
          content:"At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
            id: 2,
          name: "tony stark ",

          specialist: "Cardiologist ",
          image: "/img/doctor-2.jpg",
          content:"At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
        {
            id: 3,
          name: "anna smith",

          specialist: "Nurse Practitioner ",
          image: "/img/doctor-3.jpg",
          content:"At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
h1 {
  color: black;
}
</style>
