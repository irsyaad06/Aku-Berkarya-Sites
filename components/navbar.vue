<template>
  <v-app-bar
    fixed
    class="elevation-0"
    :class="scrollY < 10 ? 'transparent' : 'transparent'"
    height="100px"
  >
    <v-container class="d-flex justify-space-between align-center mt-6">
      <router-link to="/Contact" class="nav-link"> <p class="d-flex justify-start">KONTAK</p> </router-link>

      <router-link to="Members" class="nav-link"> <p class="d-flex justify-center">ANGGOTA</p> </router-link>

      <router-link to="/" class="nav-link">
        <v-img class="imghover" src="logo.png" max-width="90px"></v-img>
      </router-link>

      <router-link to="Events" class="nav-link"> <p class="d-flex justify-center">KEGIATAN</p></router-link>

      <router-link to="/Gallery" class="nav-link"> <p class="d-flex justify-end">GALERI</p></router-link>
    </v-container>
    <!-- <v-menu
      transition="slide-y-transition"
      bottom
      offset-y
      
    >
      <template #activator="{ on, attrs }">
        <v-btn
          class="hidden-sm-and-up"           
          icon
          v-bind="attrs"
          v-on="on"
          
        >
          <v-icon :class="scrollY < 10 ? 'white--text' : 'black--text'" >mdi-menu</v-icon>
        </v-btn>
      </template>
      <v-list>
        <v-list-item
          v-for="(menu, i) in menus"
          :key="i"
          :href="menu.link"
          dense
        >
          <v-list-item-icon>
            <v-icon>{{ menu.icon }}</v-icon>
          </v-list-item-icon>
          <v-list-item-title>{{ menu.title }}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-menu> -->
  </v-app-bar>
</template>





<script>
export default {
  data() {
    return {
      windowHeight: 0,
      scrollY: 0,
      myIcon: 'mdi-menu',
      current: 1,
      stuff: ['Home', 'Member', 'Gallery', 'Contact'],
      menus: [
        { title: 'KONTAK', icon: '', link: '/Contact' },
        { title: 'ANGGOTA', icon: '', link: '/Members' },
        { title: 'BERANDA', icon: '', link: '/' },
        { title: 'GALERI', icon: '', link: '/Gallery' },
        { title: 'KEGIATAN', icon: '', link: '/Events' },
      ],
    }
  },

  beforeMount() {
    window.addEventListener('scroll', this.handleScroll)
    window.addEventListener('resize', this.handleHeight)
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll)
    window.removeEventListener('resize', this.handleHeight)
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY
    },
    onScroll() {
      this.scrollInvoked++
    },
    handleHeight() {
      this.windowHeight = window.innerHeight
    },
  },
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,200;1,100&family=Raleway:wght@200&display=swap');

.nav-link {
  display: inline;
  font-size: 15px;
  cursor: pointer;
  transition: 0.5s;
  font-family: Poppins;
  font-weight: 200;
  letter-spacing: 1px;
  text-decoration: none;
  width: 10%;
}
.nav-link p {
  color: aliceblue;
  margin-bottom: 0px;
  display: flex;
  text-align: justify;
}
.nav-link:hover {
  font-size: 20px;
  transition: all 0.5s;
  z-index: 10;
  font-family: PoppinsLight;
}
.imghover{
  transition: 0.5s;
}
.imghover:hover{
transform: scale(1.2); 
transition: 0.5s;
}
a.nuxt-link-exact-active{
  font-size: 21px;
  font-family: PoppinsLight;
}

</style>









