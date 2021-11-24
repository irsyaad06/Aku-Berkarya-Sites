<template>
  <v-app-bar
    fixed
    elevate-on-scroll
    class="elevation-3"
    :class="scrollY < 10 ? 'transparent' : 'white'"
    height="80px"
  >
    <v-container class="d-flex">
      <v-toolbar-items class="pt-2">
        <a
          href="/"
          style="text-decoration: none"
          
          :class="scrollY < 10 ? 'white--text' : 'black--text'"
        >
          <v-img
            src="logo.png"
            max-width="90px"
            :class="scrollY < 10 ? 'appear' : 'disappear'"
          ></v-img>

          <v-img
            src="logo2.png"
            max-width="90px"
            class="mt-n15"
            :class="scrollY < 10 ? 'disappear' : 'appear'"
          ></v-img>
        </a>
      </v-toolbar-items>

      <v-spacer></v-spacer>

      <v-toolbar-items
        v-for="(menu, key) in menus"
        :key="key"
        class="hidden-xs-only"
      >
        <v-btn
          small
          text
          :class="scrollY < 10 ? 'white--text' : 'black--text'"
          :href="menu.link"
          class="py-7 ml-6"
        >
        <font size="2">  {{ menu.title }} </font>
        </v-btn>
      </v-toolbar-items>
    </v-container>
    
     <v-menu
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
    </v-menu>
  </v-app-bar>
</template>





<script>
export default {
  data() {
    return {
      windowHeight: 0,
      scrollY: 0,
      myIcon: 'mdi-menu',
      menus: [
        { title: 'Home', icon: 'mdi-home', link: '/' },
        { title: 'Member', icon: 'mdi-account-group', link: '/member' },
        { title: 'Gallery', icon: 'mdi-cast-education', link: '/galeri' },
        { title: 'Events', icon: 'mdi-cast-education', link: '/events' },
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
  mounted() {
    this.$nextTick(function () {
      this.windowHeight = window.innerHeight
    })
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

    checkLength(index) {
      if (index < this.types.length - 1) {
        index = index + 1
        return index
      }
    },
  },
}
</script>

<style>
::selection {
  background: rgb(210, 34, 34);
}
.appear {
  opacity: 1;
}
.disappear {
  
  opacity: 0;
}

.ctransparent{
  
  color: transparent;
}
.cwhite{
  animation-delay: 10s;
  background-color: white;
  color: aqua;
}
</style>








