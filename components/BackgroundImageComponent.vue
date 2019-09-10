<template>
    <v-card flat :style="style">

      <div class="overlay">
      </div>

      <div class="overlay-container">
        <v-container ma-0 fill-height row wrap>

          <div
            data-aos="fade-left"
            data-aos-delay="600"
            class="fill-height contentContainer"
            :style="contentContainerStyle"
          ></div>

          <v-layout style="z-index: 1" px-12 row wrap align-center>
            <slot></slot>
          </v-layout>
        </v-container>
      </div>

    </v-card>
</template>

<script>
    export default {
        name: "BackgroundImageComponent",
      data(){
          return{
            overlay: true
          }
      },
        props: {
            src: {
              default: '/v.png',
              value: String
            },

          position: {
            default: 'left',
            value: String
          },

          backgroundColor: {
            default: 'white',
            value: String
          },

          contentContainerStyle: {
              value: Object,
              default: () => {
                return {}
              }
          }
        },
      computed: {
          style(){
            return {
              background: this.src ? `url(${this.src}) no-repeat` : 'white',
              'back-ground-size': '100px',
              'background-color': this.backgroundColor, //use vuetify color here
              'background-position': this.position,
            }
          },
      }
    }
</script>

<style scoped>
  .overlay-container{
    position: absolute; top: 0; bottom: 0; left: 0; width: 100%;
    display: flex;
    flex: 1;
    flex-direction: column;
    justify-content: center;
  }

  .contentContainer{
    position: absolute;
    left: 0;
    right: 0;
    width: 100%;
    z-index: 0
  }

  .overlay{
    height: 100%;
    width: 100%;
    z-index: 0;
    background: rgba(255, 255, 255, 0.9);
  }

</style>
