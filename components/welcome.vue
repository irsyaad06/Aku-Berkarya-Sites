<template>
  <!-- Home First Content Start -->
  <div id="bg" style="height: 100vh;" >
    <v-container fill-height>
      <v-row class="mx-1 mt-10 mx-sm-9 mx-md-auto" style="color:white;">
        <v-col > 
          <h1 class="header text-sm-h3 font-weight-light">
            Selamat Datang di
            <br/>
            Aku berkarya
          </h1>
          <br />
          <h2 class="text-body-1 font-weight-thin">
            Mau bergabung bersama kami?
            <br />
            klik tombol dibawah ini yuk!
          </h2>
          <br />
          <v-btn elevation="2" rounded color="red" medium> <font style="color:white;" class="font-weight-light"> Gabung </font></v-btn>
        </v-col>
      </v-row>
      
    </v-container>
  </div>
  <!-- Home First Content End -->
</template>
<style>
#bg {
  background-image: linear-gradient(to bottom right, #272727, #121212);
  box-shadow: 0 17px 22px 0 rgba(0, 0, 0, 0.2), 0 20px 30px 0 rgba(0, 0, 0, 0.19);
}

@media (max-width:320px) {
  .header{
    font-size:40px;
    line-height:43px;
  }
  
}
</style>