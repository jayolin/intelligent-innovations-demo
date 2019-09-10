<template>
  <v-app light>
    <!-- App Toolbar -->
    <app-toolbar></app-toolbar>

    <!-- App Content -->
    <v-content>
      <v-container pa-0>
        <nuxt />
      </v-container>
    </v-content>

    <!-- App Footer -->
    <app-footer></app-footer>
  </v-app>
</template>

<script>

import AppFooter from "~/components/layouts/AppFooter"
import AppToolbar from "~/components/layouts/AppToolbar"

export default {
  data () {
    return {

    }
  },
  components: {
    AppFooter, AppToolbar
  }
}
</script>
<style>
  *{
    font-family: Geneva,serif;
  }
</style>
