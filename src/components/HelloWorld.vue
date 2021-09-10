<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        <v-avatar size="200">
          <img class="my-3" src="../assets/osaka.jpg" alt="獅子" />
        </v-avatar>
      </v-col>

      <v-col class="mb-4">
        <h1 class="display-2 font-weight-bold mb-3">
          Welcome to <span>My-First-Vue</span>
        </h1>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "HelloWorld",
};
</script>
<style scoped>
span {
  background-color: darkgreen;
  color: white;
  padding: 5px;
}
</style>
