<template>
  <div>
    <v-app-bar
      fixed
      class="elevation-0 mx-sm-7"
      :class="scrollY < 10 ? 'transparent' : 'transparent'"
      height="100px"
    >
      <v-container
        class="d-none d-sm-flex justify-space-between align-center mt-6"
      >
        <router-link to="/Contact" class="nav-link">
          <p class="d-flex justify-start">KONTAK</p>
        </router-link>

        <router-link to="Members" class="nav-link">
          <p class="d-flex justify-center">ANGGOTA</p>
        </router-link>

        <router-link to="/" class="nav-link">
          <v-img class="imghover" src="logo.png" max-width="90px"></v-img>
        </router-link>

        <router-link to="Events" class="nav-link">
          <p class="d-flex justify-center">KEGIATAN</p></router-link
        >

        <router-link to="/Gallery" class="nav-link">
          <p class="d-flex justify-end">GALERI</p></router-link
        >
      </v-container>

      <v-container class="navbar-resp hidden-sm-and-up">
        <router-link to="/" class="">
          <v-img class="" src="logo.png" max-width="70px"></v-img>
        </router-link>

        <v-btn
          class="hidden-sm-and-up"
          icon
          @click="drawer = !drawer"
          style="z-index: 100000000000000"
        >
          <v-icon large>mdi-menu-open</v-icon>
        </v-btn>
      </v-container>
    </v-app-bar>

    <v-navigation-drawer
      class="hidden-sm-and-up"
      v-model="drawer"
      absolute
      height="100vh"
      width="200px"
      style="z-index: 100000"
      :value="close"
    >
    <v-list-item  class="mx-3">

      <v-avatar class="mr-1" color="#FC5D4C" size="10"></v-avatar>

      <v-avatar class="mr-1" color="#FFBE38" size="10"></v-avatar>

      <v-avatar class="mr-1" color="#65E14C" size="10"></v-avatar>
    </v-list-item>
      <v-list-item class="ml-3">
        <v-avatar class="my-2 rounded-lg" rounded size="40">
          <v-img src="logo-back-w.png"></v-img>
        </v-avatar>
      </v-list-item>

      <v-list  nav class="mt-2">
        <v-list-item
          style="height: 1px"
          v-for="(menu, i) in menus"
          :key="i"
          nuxt
          :to="menu.link"
        >
          <v-list-item-icon class="mr-1 my-2 mt-3 ml-3">
            <router-link class="text-decoration-none mx-0" :to="menu.link">
              <v-icon color="white" small>{{ menu.icon }}</v-icon>
            </router-link>
          </v-list-item-icon>

          <v-list-item-content class="py-0">
            <v-list-item-title>
              <router-link
                class="nav-link text-decoration-none"
                :to="menu.link"
              >
                <p class="pt-1" style="font-size: 13px; letter-spacing: 0px">
                  {{ menu.title }}
                </p>
              </router-link>
            </v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>





<script>
export default {
  data() {
    return {
      myIcon: 'mdi-menu',
      drawer: null,
      close: true,
      menus: [
        { title: 'Beranda', icon: 'mdi-home-outline', link: '/' },
        {
          title: 'Anggota',
          icon: 'mdi-account-group-outline',
          link: '/Members',
        },
        { title: 'Kegiatan', icon: 'mdi-calendar-multiple', link: '/Events' },
        { title: 'Galeri', icon: 'mdi-image-outline', link: '/Gallery' },
        { title: 'Kontak', icon: 'mdi-contacts-outline', link: '/Contact' },
      ],
    }
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
.imghover {
  transition: 0.5s;
}
.imghover:hover {
  transform: scale(1.2);
  transition: 0.5s;
}
.overlay {
  background-color: red;
}
.navbar-resp {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  width: 100%;
  max-width: 1024px;
}
@media (min-width: 600px) {
  a.nav-link.nuxt-link-exact-active {
    font-size: 21px;
    font-family: PoppinsLight;
  }
  .imghover {
    transition: 0.5s;
  }
}
</style>









