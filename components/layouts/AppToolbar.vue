<template>
  <v-app-bar
    color="transparent"
    light
    absolute
    class="px-4"
    flat
  >

    <v-toolbar-title data-aos="fade-left">
      <img height="20" contain src="/logo.png"/>
    </v-toolbar-title>
    <v-spacer></v-spacer>
    <v-toolbar-items>
      <v-btn
        data-aos="fade-left"
        :data-aos-delay=" (i + 3) *  100"
        small  :to="item.to" :key="`navigation-item-${i}`" text v-for="(item, i) in items">
        {{item.title}}
      </v-btn>
    </v-toolbar-items>

  </v-app-bar>
</template>

<script>
    import AOS from 'aos'
    export default {
        name: "AppToolbar",
        data(){
          return {
            items: [
              {
                title: 'SHOP',
                to: '/shop'
              },
              {
                title: 'WHOLESALE',
                to: '/wholesale'
              },
              {
                title: 'LOCATIONS',
                to: '/locations'
              },
              {
                title: 'OUR STORY',
                to: '/our-story'
              },
            ]
          }
        },
        mounted(){
          AOS.init()
        },
    }
</script>

<style scoped>

</style>
