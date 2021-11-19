<template>

  <v-app>

    <v-main>

      <v-container>
        <navbar/>
        <Nuxt />
      </v-container>
    </v-main>
   
    <v-footer
      :absolute="!fixed"
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
