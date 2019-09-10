<template>
  <v-layout
    row wrap
  >
    <v-flex xs12>

      <header-component/>
      <details1/>
      <details2/>
      <details3/>

    </v-flex>
  </v-layout>
</template>

<script>

import HeaderComponent from "../components/Header"
import Details1 from "../components/Details1";
import Details2 from "../components/Details2";
import Details3 from "../components/Details3";

export default {
  components: {Details3, Details2, Details1, HeaderComponent},
  data(){
    return{
      contentContainerStyle: {
        'background-image': 'url("/coffee-cup.png")',
        'background-repeat': 'no-repeat',
        'background-position': 'right',
        'background-size': 'contain'
      },
      items: [
        {
          icon: 'brightness_high',
          desc: 'Quality coffee cultivated by good',
          fancy: true
        },
        {
          icon: 'new_releases',
          desc: 'Milk grounds chicory bean single origin'
        },
        {
          icon: 'local_florist',
          desc: 'Flavour single origin froth in spoon iced',
        },
        {
          icon: 'waves',
          desc: 'Coffee irish robusta spoon robust',
        },
      ],
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
<style>
  .stuff{

  }
</style>
