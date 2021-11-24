<template>
  <div>
    <!-- Home First Content Start -->
    <div style="height: 100vh">
      <link rel="preconnect" href="https://fonts.googleapis.com" />
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
      <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@200&display=swap" rel="stylesheet"/>
      <v-container fill-height>
        <v-row>
          <v-col>
            <h1 class="text-h3 font-weight-light" 
                style="font-family: Raleway"
            >
              Selamat Datang di 
              <br/> 
              Aku berkarya
            </h1>
            <br/>
            <h2 class="text-body-1 font-weight-thin"
            >
              Mau bergabung bersama kami? 
              <br/>
              klik tombol dibawah ini yuk!
            </h2>
            <br>
            <v-btn 
            elevation="2" 
            rounded
            color="red"
            medium
            >
              Join us
            </v-btn>
          </v-col>
        </v-row>
      </v-container>
    </div>
    <!-- Home First Content End -->

    <!-- Home Second Content Start -->
    <div style="height:auto; background-color:red;"
         
    >
      <h1 class="d-flex justify-center mb-16 " >Follow us</h1>
      <v-row>
        <v-col align="center">
            YOUTUBE
            <v-img src="/youtube.ico"
                   max-width="200px"></v-img>
        </v-col>
        <v-col align="center">
            INSTAGRAM
            <v-img src="/instagram.png"
                   max-width="200px"></v-img>
        </v-col>
      </v-row>
    </div>
    <!-- Home Second Content End -->
  </div>
</template>

<script>
export default {
  setup() {
    
    },
   head() {
     return {
       title: 'Home',
      overlay: false,
    }
  },
}
</script>
