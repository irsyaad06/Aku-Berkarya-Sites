<template>
      <!-- Home Second Content Start -->
        <v-container style="height:100vh;" class="mb-16-md">
              <v-row align="center">
                <v-col md="4" :order="$vuetify.breakpoint.smAndDown ? first  : 'last'">
                  <v-img src="aboutus.svg" 
                  :width="$vuetify.breakpoint.mdAndDown ? 300  : '400'"
                
                   ></v-img>
                </v-col>
                <v-col sm=5>
                    <h1 class="font-weight-medium"
                        style="font-size:40px;"> Tentang <font class="backwar"> Kami </font></h1>
                   <br>
                    <v-contenttitle > Aku berkarya adalah sebuah komunitas yang dibentuk untuk mengumpulkan pemuda pemudi indonesia untuk berkumpul dan membuat karya bersama khususnya dalam bidang dakwah </v-contenttitle>
                </v-col>
                    <v-col class="hidden-xs-only"></v-col>

                
              </v-row>
        </v-container>

    <!-- Home Secong Content End -->
</template>


<style>
 .backwar{
    display: inline-block;
    line-height: 0.55;
    border-bottom: 7px solid #d22222;
}
</style>