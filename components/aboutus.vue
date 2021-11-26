<template>
      <!-- Home Second Content Start -->
        <v-container style="height:auto;" >
              <v-row align="center">
                <v-col md="4" :order="$vuetify.breakpoint.smAndDown ? first  : 'last'">
                  <v-img src="aboutus.svg" 
                  :width="$vuetify.breakpoint.mdAndDown ? 300  : '400'"
                class="mb-auto mb-xs-16"
                   ></v-img>
                </v-col>
                <v-col sm=5>
                    <h1 class="font-weight-medium"
                        style="font-size:40px;"> Info <font class="backwar"> Komunitas </font></h1>
                   <br>
                    <v-contenttitle> <v-bold class="font-weight-bold"> Aku berkarya </v-bold> merupakan komunitas yang mewadahi kreatifitas anak-anak muda untuk berkarya serta mengasah skill dan bakat yang dimiliki. Diawali dengan film pendek berjudul 'Murid Ngaji' pada tahun 2018 kemudian dilanjut oleh karya karya lainnya. Aku berkarya resmi menjadi komunitas pada tanggal 24 November 2019, dan terus berjalan hingga saat ini. </v-contenttitle>
                </v-col>
                    <v-col class="hidden-xs-only"></v-col>

                
              </v-row>
        </v-container>

    <!-- Home Secong Content End -->
</template>


<style>
 .backwar{
    display: inline-block;
    line-height: 0.42;
    border-bottom: 7px solid #d22222;
}
</style>