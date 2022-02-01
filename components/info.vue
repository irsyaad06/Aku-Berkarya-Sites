<template>
  <!-- Home Third Content Start -->
  <v-container fluid class="pa-0" style="background-color: white">
    <v-container style="height: 85vh; color: #121212" fill-height>
      <v-row class="mx-1 mx-sm-9 mx-md-auto">
        <v-col cols="12" sm="9" md="6">
          <h1 class="text-h2 font-weight-medium">Info</h1>
          <h1 class="text-h3 font-weight-light">
            Aku <font style="color: #f44336">Berkarya</font>
          </h1>
          <br />
          <v-alert
            border="left"
            colored-border
            color="#f44336"
            elevation="0"
            class="font-weight-light py-2"
          >
            <font class="font-weight-medium"> Aku berkarya </font>merupakan
            komunitas yang mewadahi kreatifitas anak-anak muda untuk berkarya
            serta mengasah skill dan bakat yang dimiliki. Diawali dengan film
            pendek berjudul
            <font class="font-weight-medium"> 'Murid Ngaji' </font> pada tahun
            2018 kemudian dilanjut oleh karya karya lainnya. Aku berkarya resmi
            menjadi komunitas pada tanggal 24 November 2019, dan terus berjalan
            hingga saat ini.
          </v-alert>

           <div class="d-flex justify-start align-center mt-4">
          <h5 class="mr-1">Ikuti kami</h5>

          <a
            :href="smediaa.link"
            target="blank"
            v-for="(smediaa, i) in smedia"
            :key="i"
          >
            <v-img :src="smediaa.image" max-width="20px" class="gambar mx-1">
            </v-img
          ></a>
        </div>
        </v-col>

        <v-col cols="12" sm="10" md="8" lg="6">
          <v-carousel
            cycle
            interval="2800"
            height="310"
            hide-delimiter-background
            :show-arrows="false"
            class="mt-0"
          >
            <v-carousel-item v-for="(slide, i) in slides" :key="i">
              <v-img max-width="550px" :src="slide"></v-img>
            </v-carousel-item>
          </v-carousel>
        </v-col>
       
      </v-row>
    </v-container>
  </v-container>
  <!-- Home Third Content End -->
</template>

<script>
export default {
  data() {
    return {
      smedia: [
        {
          image: 'youtube.png',
          title: 'Youtube',
          link: 'https://youtube.com/c/AkuBerkaryaOfficial',
        },
        {
          image: 'instagram.png',
          title: 'Instagram',
          link: 'https://www.instagram.com/aku.berkarya/?hl=id',
        },
        {
          image: 'tiktok.png',
          title: 'TikTok',
          link: 'https://t.tiktok.com/i18n/share/user/6868845549546767362/?_d=d6kbf8ibah6dha&language=id&sec_uid=MS4wLjABAAAA1tcUOIcdfzFYnMB9ZWF24vWOfZ98lkdXdERAbuV9phFA2QVllprHdNnKRsf0THoI&share_author_id=6868845549546767362&u_code=dea0m4j9ia9aj1&timestamp=1637733618&user_id=6868845549546767362&sec_user_id=MS4wLjABAAAA1tcUOIcdfzFYnMB9ZWF24vWOfZ98lkdXdERAbuV9phFA2QVllprHdNnKRsf0THoI&utm_source=copy&utm_campaign=client_share&utm_medium=android&share_iid=7024669315999893275&share_link_id=312d31b6-e3dc-433d-996b-06a5cc2d81c4&share_app_id=1180',
        },
        {
          image: 'snackvideo.png',
          title: 'Snack Video',
          link: 'http://m.snackvideo.com/user/150000601370771?fid=150000601370771&cc=share_copylink&language=in-id&share_device_id=ANDROID_aab889df0849a57f&share_id=ANDROID_aab889df0849a57f_1637733658295&share_uid=150000601370771&timestamp=1637733658295&share_item_type=profile',
        },
      ],

      slides: ['mn.jpg', 'manga.jpg', 'aars.jpg', 'pb.jpg', 'tam.jpg'],
    }
  },
}
</script>

<style>
.gambar {
  transition: 0.2s;
}

.gambar:hover {
  transform: scale(1.2);
  transition: 0.2s;
}
</style>