<template>
  <!-- Home Second Content Start -->
  <v-container
    id="kegiatan"
    fluid
    style="
      height: 100vh;
      box-shadow: 0 -200px 100px 0 rgba(0, 0, 0, 0.2),
        0 0px 20px 0 rgba(0, 0, 0, 0.19);
    "
  >

  <carousel-3d>
  <slide :index="0">
    Slide 1 Content
  </slide>
  <slide :index="1">
    Slide 2 Content
  </slide>
  <slide :index="2">
    Slide 2 Content
  </slide>
  <slide :index="3">
    Slide 2 Content
  </slide>
  <slide :index="4">
    Slide 2 Content
  </slide>
</carousel-3d>

<carousel-3d>
    <slide v-for="(slide, i) in slides" :index="i" :key="i">
        <template slot-scope="{ index, isCurrent, leftIndex, rightIndex }">
            <img :data-index="index" :class="{ current: isCurrent, onLeft: (leftIndex >= 0), onRight: (rightIndex >= 0) }" :src="slide.src">
        </template>
    </slide>
</carousel-3d>

  </v-container>

  <!-- Home Secong Content End -->
</template>

<script>
export default {
  data() {
    return{

      slides:7 
    }
  },
  components: {
  }
}
</script>

<style>
.carousel-3d-container figure {
  margin:0;
}

.carousel-3d-container figcaption {
  position: absolute;
  background-color: rgba(0, 0, 0, 0.5);
  color: #fff;
  bottom: 0;
  position: absolute;
  bottom: 0;
  padding: 15px;
  font-size: 12px;
  min-width: 100%;
  box-sizing: border-box;
}
</style>