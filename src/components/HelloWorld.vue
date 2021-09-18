<template>
  <v-container fill-height>
    <v-row class="text-center" align-content="center">
      <v-col cols="12">
        <VueSlickCarousel
          :arrows="true"
          :dots="false"
          :autoplay="true"
          :autoplaySpeed="5000"
        >
          <div>
            <v-avatar size="200"
              ><img src="../assets/osaka.jpg" alt="獅子丸"
            /></v-avatar>
          </div>
          <div>
            <v-avatar size="200"
              ><img src="../assets/fukui.png" alt="レッサー君"
            /></v-avatar>
          </div>
          <div>
            <v-avatar size="200"
              ><img src="../assets/panda.jpg" alt="パンダ"
            /></v-avatar>
          </div>
        </VueSlickCarousel>
      </v-col>
      <v-col class="mb-4">
        <div class="d-flex justify-center">
          <h1 class="hidden-md-and-down">Welcome to</h1>
          <h1>
            <span
              >My-First-<font-awesome-icon :icon="['fab', 'vuejs']" />ue</span
            >
          </h1>
        </div>
        <h2>The Grand Experiment(-)</h2>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import VueSlickCarousel from "vue-slick-carousel";
import "vue-slick-carousel/dist/vue-slick-carousel.css";
// optional style for arrows & dots
import "vue-slick-carousel/dist/vue-slick-carousel-theme.css";
export default {
  name: "HelloWorld",
  components: { VueSlickCarousel },
};
</script>
<style scoped>
span {
  background-color: darkgreen;
  color: white;
  padding: 5px;
}
</style>
