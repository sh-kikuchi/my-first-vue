<template>
  <div id="app">
    <v-app>
      <v-app-bar color="dark" dark app>
        <v-toolbar-title>My First Vue.</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items>
          <v-btn text color="white"
            ><router-link style="text-decoration: none; color: white" to="/"
              >@HOME</router-link
            ></v-btn
          >
          <v-btn text
            ><router-link style="text-decoration: none; color: white" to="/list"
              >ListS</router-link
            ></v-btn
          >
          <v-btn text
            ><router-link
              style="text-decoration: none; color: white"
              to="/color"
              >ColorS</router-link
            ></v-btn
          >
          <v-btn text
            ><router-link style="text-decoration: none; color: white" to="/book"
              >BookS</router-link
            ></v-btn
          >
          <v-menu offset-y>
            <template v-slot:activator="{ on }">
              <v-btn v-on="on" text
                ><router-link
                  style="text-decoration: none; color: white"
                  to="/work"
                  >WorkS</router-link
                ></v-btn
              >
            </template>
            <!-- <v-list>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title
                    ><v-btn text>Private Works</v-btn></v-list-item-title
                  >
                </v-list-item-content>
              </v-list-item>
              <v-list-item>
                <v-list-item-content>
                  <v-list-item-title
                    ><v-btn text>Business</v-btn></v-list-item-title
                  >
                </v-list-item-content>
              </v-list-item>
            </v-list> -->
          </v-menu>
        </v-toolbar-items>
      </v-app-bar>
      <v-main>
        <router-view />
      </v-main>
      <v-footer class="footer" dark app>
        <div class="footer">Sometimes the best gain is to lose</div></v-footer
      >
    </v-app>
  </div>
</template>

<script>
export default {
  name: "App",
};
</script>
<style>
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
