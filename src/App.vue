<template>
<div>
  <v-app class="overflow-hidden">
    <v-app-bar dark app>
        <v-toolbar-title class="hidden-md-and-down">My First Vue.</v-toolbar-title>
        <v-tabs align-with-title>
          <v-tab>
            <router-link style="text-decoration: none; color: white" to="/">@HOME</router-link>
          </v-tab>
          <v-tab>
            <router-link style="text-decoration: none; color: white" to="/work">WorkS</router-link>
          </v-tab>
          <v-tab>
            <router-link style="text-decoration: none; color: white" to="/list">ListS</router-link>
          </v-tab>
          <v-tab>
            <router-link style="text-decoration: none; color: white" to="/color">ColorS</router-link>
          </v-tab>
          <v-tab>
           <router-link style="text-decoration: none; color: white" to="/book">BookS</router-link>
          </v-tab>
        </v-tabs>
    </v-app-bar>
    <v-main>
      <router-view />
    </v-main>
  </v-app>
  <v-footer class="footer" dark app>
    <div class="footer">Sometimes the best gain is to lose</div>
  </v-footer>
</div>

</template>
<script>
  export default {
    name: "App",

  }
</script>
<style>
.v-toolbar__title {
  overflow: visible !important;
  margin-right: 50px !important;
}
.page-title,
.page-sub-title {
  text-align: center;
}

.contents {
  margin: 0 auto;
}
.footer {
  margin: 0 auto;
}
</style>
