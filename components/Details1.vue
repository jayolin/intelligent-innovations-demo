<template>
  <background-image-component
    :src="null"
    style="height: 350px; overflow: hidden"
  >
    <v-flex
      data-aos="fade-left"
      :data-aos-delay=" (i + 1) * 100"
      v-for="(item, i) in items"
      :key="`items-${i}`" xs3>

      <div :class="[{'primary lighten-5': item.fancy}, 'px-4']" style="border-radius: 0 30px 0 0;overflow: hidden;position:relative;padding-top: 30px; height: 220px; width: 200px">
        <v-avatar v-if="item.fancy" color="primary" size="350" style="position: absolute; top: -265px; left: -40%; z-index: 0 !important;"></v-avatar>
        <div style="z-index: 999 !important; position: relative">
          <v-icon large>{{item.icon}}</v-icon>
          <div class="mt-7 font-weight-light" style="line-height: 1.2">{{item.desc}}</div>
        </div>

      </div>

    </v-flex>
  </background-image-component>
</template>

<script>
  import BackgroundImageComponent from "../components/BackgroundImageComponent";
  import AOS from 'aos'
  export default {
    name: "Details1",
    components: {BackgroundImageComponent},
    mounted(){
      AOS.init()
    },
    data(){
      return{
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
            icon: 'aspect_ratio',
            desc: 'Coffee irish robusta spoon robust',
          },
        ]
      }
    }
  }
</script>

<style scoped>

</style>
