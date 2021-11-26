<template>
  <!-- Home Third Content Start -->
  <v-container fluid class="pa-0 ">
    <div style="height:auto; background-color: #1f1f1f" class="pb-16 pt-16">
      <v-container>
        <h1 class="text-center">Ikuti <font class="backwar">Kami</font> </h1>
        <v-sub
          class="d-flex justify-center text-center text-body-1 font-weight-light mb-16"
        >
          Kami memiliki Social Media yang dijadikan tempat untuk berkarya, cek
          yu!
        </v-sub>

        <v-row>
          <v-col v-for="(smediaa, key) in smedia" :key="key" align="center">
          <v-img :src="smediaa.image" max-width="50px" class="mb-1"> </v-img>
            <h1 class="text-h5 font-weight-light">{{ smediaa.title }}</h1>
            <v-subtitle class=""> {{ smediaa.vsub }} 
           
            <v-btn  :href="smediaa.link" 
                    target="blank"
                    rounded
                    color="rgba(240, 14, 14, .4)"
                    small
                    class="mt-2"
                    > Selengkapnya</v-btn>
            </v-subtitle>
          </v-col>
        </v-row>
      </v-container>
    </div>
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
    }
  },
}
</script>
