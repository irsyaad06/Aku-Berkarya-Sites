<template>

  <v-app>

    <v-main>

      <v-container fluid class="pa-0">
        <navbar/>
        <Nuxt />
      </v-container>

    </v-main>
   
    <v-footer
      app
      class="d-flex justify-center"
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
    
     
    }
  }
}
</script>
