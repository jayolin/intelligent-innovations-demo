<template>

  <div>
    <div style="background: #333" class="pa-12 text-center white--text">

      <div data-aos="fade-up">
        <div class="headline font-weight-light">Would you like to hear from us?</div>
        <div class="caption mt-3">Submit your email for our newsletter</div>
        <v-text-field class="mx-auto" style="width: 250px; display: block;" dark placeholder="yourname@mail.com"></v-text-field>

      </div>

    </div>
    <v-footer dark>
      <span>&copy; 2019</span>
    </v-footer>
  </div>


</template>

<script>
    import AOS from 'aos'
    export default {
        name: "AppFooter",
        mounted(){
          AOS.init()
        },
    }
</script>

<style scoped>

</style>
