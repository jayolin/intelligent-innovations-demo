<template>
  <background-image-component background-color="#EEDC82" :content-container-style="contentContainerStyle" style="height: 420px; overflow: hidden">
    <v-flex xs12>
      <div style="width: 40%">
        <div
          data-aos="fade-up"
        >
          <h5 class="font-weight-light mb-1">PREMIUM COFFEE</h5>
          <h1 style="line-height: 1.1" class="font-weight-bold">A cup of coffee is one of the most important, simple pleasures in life.</h1>
        </div>

        <custom-button
          data-aos="fade-up"
          data-aos-delay="300"
          class="mt-5"
        >
          Shop Now
        </custom-button>

      </div>

    </v-flex>
  </background-image-component>
</template>

<script>
  import BackgroundImageComponent from "../components/BackgroundImageComponent";
  import AOS from 'aos'
  import CustomButton from "./CustomButton";
  export default {
    name: "Header",
    components: {CustomButton, BackgroundImageComponent},
    mounted(){
      AOS.init()
    },
    data(){
      return{
        contentContainerStyle: {
          'background-image': 'url("/coffee-cup.png")',
          'background-repeat': 'no-repeat',
          'background-position': 'right',
          'background-size': 'contain'
        }
      }
    }
  }
</script>

<style scoped>

</style>
