<template>
  <v-app-bar
    fixed
    class="elevation-0"
    :class="scrollY < 10 ? 'transparent' : 'transparent'"
    height="100px"
  >
    <v-container class="d-flex justify-space-between align-center">
      <!-- <v-toolbar-items class="pt-2">
        <a
          href="/"
          style="text-decoration: none"
          
          :class="scrollY < 10 ? 'white--text' : 'white--text'"
        >
          <v-img
            src="logo.png"
            max-width="90px"
            :class="scrollY < 10 ? 'appear' : 'appear'"
          ></v-img>

          <v-img
            src="logo2.png"
            max-width="90px"
            class="mt-n15"
            :class="scrollY < 10 ? 'disappear' : 'disappear'"
          ></v-img>
        </a>
      </v-toolbar-items> -->
      <div
        v-for="rlink, i in menus"
        :key="i"
        class="d-none d-sm-none d-md-flex"
      >
        <router-link
          class="nav-link text-decoration-none"
          :to="rlink.link"
        >
         <p> {{ rlink.title }} </p>
        </router-link>
      </div>
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

a {
  display: inline;
  padding: 15px;
  font-size: 15px;
  color: white;
  cursor: pointer;
  transition: 0.5s;
  font-family: Poppins;
  font-weight: 200;
  letter-spacing: 1px;
}
a:hover {
  font-size: 20px;
  transition: all 0.5s;
  z-index: 10;
  font-family: PoppinsLight;
}
a.nuxt-link-exact-active{
  font-size: 22px;
  font-family: PoppinsLight;
}
p{
  color: aliceblue;
}
</style>









