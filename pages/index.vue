<template>
  <div>
    <!-- Home First Content Start -->
    <div style="height: 100vh">
      <link rel="preconnect" href="https://fonts.googleapis.com" />
      <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
      <link href="https://fonts.googleapis.com/css2?family=Raleway:wght@200&display=swap" rel="stylesheet"/>
      <link href="https://use.fontawesome.com/releases/v5.0.13/css/all.css" rel="stylesheet">
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
        <v-container style="height:100vh;">
              <v-row>
                <v-col>
                   <v-title class="text-h2" style="background-color:red; backgrp"> Tentang Kami</v-title>
                   <br>
                   <br>
                    <v-contenttitle> Lorem Ipsum is simply dummy text of the printing and typesetting industry. <br> Lorem Ipsum has been the industry's standard dummy text ever since the 1500s </v-contenttitle>
                </v-col>
                <v-col sm=4>
                  <v-img src="aboutus.svg"></v-img>
                </v-col>
              </v-row>
        </v-container>

    <!-- Home Secong Content End -->

    <!-- Home Third Content Start -->
    <v-container 
        fluid 
        class="pa-0" 
    >
      <div 
        style="height:auto; background-color:#1f1f1f;"
      >
        <h1 class="d-flex justify-center pt-16">Ikuti Kami</h1>
        <v-sub class="d-flex justify-center text-body-1 font-weight-light mb-16"> Kami memiliki Social Media yang dijadikan tempat untuk berkarya, cek yu! </v-sub>
          <v-row>
            <v-col>
               <h1>Youtube / </h1>
              
            </v-col>
          </v-row>
        </div>
    </v-container>
    <!-- Home Third Content End -->
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
