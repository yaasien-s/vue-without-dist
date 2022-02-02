<template>
     <div v-if="testimonial" class="testimonial-details">
    <h1>{{ testimonial.name }}</h1>
    <img :src="testimonial.image" alt="" id="one">
    <p>Age: {{ testimonial.age }}</p>
    <h5 class="my-4">{{ testimonial.details }}</h5>
  </div>
  <div v-else id="preload">
      Loading testimonial data...
  </div>
    <button @click="back" id="Back">Go Back</button>
</template>
<script>
export default {
     props: ['id'],
    data() {
        return {
            testimonial: null
        }
    },
    mounted() {
        fetch('http://localhost:3000/testimonial/' + this.$route.params.id)
        .then(res => res.json())
        .then(data => {
            console.log(data);
            this.testimonial = data
        })
        .catch(err => console.log(err.message))
    },
    methods: {
         back() {
      this.$router.go(-1)
    }
    }
}
</script>
<style>
    .testimonial-details {
     background: #2b2b26;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #568259;
    margin-top: 75px;
}

.testimonial-details p {
    font-weight: 600;
}
#Back {
  margin: 0 10px;
  padding: 10px;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  background: #2b2b26;
  color: #568259;
}
#Back:hover {
    background: #568259;
    color: #2b2b26;
    border: #2b2b26 1px solid;
    font-weight: 600;
}
#preload {
    margin-top: 100px;
}
#one {
    width: 75%;
}
</style>