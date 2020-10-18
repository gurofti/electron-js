<template>
  <no-ssr placeholder="loading...">
    <carousel-3d
        :height="200"
        :width="400"
        :border="1"
        :autoplay="true"
        :autoplay-timeout="2400"
    >
      <slide v-for="(slide, i) in slides" :index="i" :key="i">
        <img v-bind:src="slide.src" alt="">
      </slide>
    </carousel-3d>
  </no-ssr>
</template>

<script>
export default {
  name: "Carousel",
  data() {
    return {
      slides: [
        { src: require('../assets/01.jpg')},
        { src: require('../assets/02.jpg')},
        { src: require('../assets/03.jpg')},
        { src: require('../assets/04.jpg')},
        { src: require('../assets/05.jpg')},
        { src: require('../assets/06.jpg')},
      ]
    }
  }
}
</script>

<style scoped>
  .carousel-3d-slide {
    height: 100% !important;
  }
</style>