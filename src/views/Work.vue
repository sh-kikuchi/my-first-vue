<template>
  <div>
    <h1>WORKS</h1>
    <VueSlickCarousel :arrows="true" :dots="true">
      <div><img src="../assets/mysite.jpg" /></div>
      <div><img src="../assets/kanban.jpg" /></div>
      <div><img src="../assets/smalltalk.jpg" /></div>
      <div><img src="../assets/bookstock.png" /></div>
    </VueSlickCarousel>
  </div>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";

export default {
  components: { VueSlickCarousel },
};
</script>
<style scoped>
img {
  width: 50%;
  height: 50%;
  margin: 0 auto;
}
</style>
