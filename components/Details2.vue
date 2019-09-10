<template>
  <background-image-component
    src="/v3.png"
    position="center center"
    style="height: 400px; overflow: hidden">
    <v-flex xs6>
      <v-avatar
        data-aos="fade-right"
        class="red" size="350">
        <v-img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRFO99MPnV5oypGuh6x3qszYsIMtGPDAeIKBOqpX9sesSQGejdW"/>
      </v-avatar>
    </v-flex>
    <v-flex xs6>
      <div data-aos="fade-up">
        <h5 class="font-weight-light mb-1">PREMIUM COFFEE</h5>
        <h2 style="line-height: 1.2">Quality Coffee<br/> Cultivated by Good</h2>
        <p class="mt-3">Our love for speciality coffee is never-ending. With over 365 days a year at origin working the best growers on the
          planet, only the best beans make the grade.</p>
      </div>

      <custom-button
        data-aos="fade-up"
        data-aos-delay="100"
      >
        Shop Now
      </custom-button>

    </v-flex>
  </background-image-component>
</template>

<script>
  import BackgroundImageComponent from "../components/BackgroundImageComponent";
  import AOS from 'aos'
  import CustomButton from "./CustomButton";
  export default {
    name: "Details2",
    components: {CustomButton, BackgroundImageComponent},
    mounted(){
      AOS.init()
    },
  }
</script>

<style scoped>

</style>
