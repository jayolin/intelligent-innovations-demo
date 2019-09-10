<template>
  <background-image-component
    src="/v3.png"
    background-color="#EEDC82"
    position="center top"
    style="height: 600px; overflow: hidden"
  >
    <v-flex>
      <div class="text-center">
        <div data-aos="fade-up">
          <h5 class="font-weight-light mb-1">BUY NOW</h5>
          <h2 style="line-height: 1.2">Our Best Deal</h2>
        </div>

        <p
          data-aos="fade-up"
          data-aos-delay="200"
          class="mt-3"
        >
          Coffee company with a straightforward mission: to make an office <br/> and on-the-go cup of coffee that we'd like
          to drink ourselves.
        </p>
      </div>
      <div>
        <v-layout row wrap>
          <v-flex mt-3 text-center :key="`product-${i}`" v-for="(product, i) in products">
            <v-img
              data-aos="fade-down"
              :data-aos-delay="(i + 3) * 100"
              contain height="200"
              aspect-ratio="3" :src="product.img"/>


            <div class="mt-3" data-aos="fade-up"
                 :data-aos-delay="(i + 3) * 150">
              <h5 class="font-weight-light mb-1">{{product.plan}}</h5>
              <h5>{{product.name}}</h5>

              <custom-button class="mt-3">
                {{product.price}}
              </custom-button>

            </div>

          </v-flex>
        </v-layout>

      </div>
    </v-flex>

  </background-image-component>
</template>

<script>
  import BackgroundImageComponent from "../components/BackgroundImageComponent";
  import AOS from 'aos'
  import CustomButton from "./CustomButton";
  export default {
    name: "Details3",
    components: {CustomButton, BackgroundImageComponent},
    mounted(){
      AOS.init()
    },
    data(){
      return{
        products: [
          {
            name: 'Noansa Platinum Blend',
            plan: 'PLATINUM',
            price: '$30.00',
            img: 'https://imageskincare.com/media/catalog/product/cache/15d40a89ecb71f34de77544d7b6bb99f/v/i/vital-c-hydrating-hand-and-body-lotion_3_1.png'
          },
          {
            name: 'Noansa Classic Blend',
            plan: 'CLASSIC',
            price: '$30.00',
            img: 'http://www.antiagr.com/wp-content/uploads/2014/04/Nerium-Firming-Body-Contouring-Cream-550-450x450.png'
          },
          {
            name: 'Noansa General Blend',
            plan: 'GENERAL',
            price: '$30.00',
            img: 'https://imageskincare.com/media/catalog/product/cache/15d40a89ecb71f34de77544d7b6bb99f/v/i/vital-c-hydrating-hand-and-body-lotion_3_1.png'
          }
        ]
      }
    }
  }
</script>

<style scoped>

</style>
