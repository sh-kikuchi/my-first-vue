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
        <h1 class="display-2 font-weight-bold mt-3 mb-3 pt-3">
          <span class="hidden-md-and-down">Welcome to</span>
          <span>My-First-<font-awesome-icon :icon="['fab', 'vuejs']" />ue</span>
        </h1>
        <h2>- The Grand Experiment(-) -</h2>
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
