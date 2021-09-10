<template>
  <div id="book">
    <h1 class="page-title">Library</h1>
    <h3 class="page-sub-title">今、読みたい本はどんなもの？</h3>
    <div>
      <v-text-field
        class="search-input"
        label="タイトルや著者で検索して下さい"
        v-model="keyword"
        hide-details="auto"
        color="success"
        loading
      ></v-text-field>
    </div>
    <div class="d-flex center">
      {{ message }}
    </div>
    <v-container>
      <v-row dense>
        <v-col v-for="(item, index) in items" :key="index" cols="4">
          <v-card height="250px">
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <a v-bind:href="item.volumeInfo.previewLink" target="_blank">
                  <img
                    class="card-image"
                    v-bind:src="item.volumeInfo.imageLinks.thumbnail"
                  />
                </a>
              </div>
              <div>
                <v-card-title class="card-title">{{
                  item.volumeInfo.title
                }}</v-card-title>
                <v-card-text card-text>{{
                  item.volumeInfo.authors
                }}</v-card-text>
                <v-card-text card-text>{{
                  item.volumeInfo.publisher
                }}</v-card-text>
              </div>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>
<script>
import axios from "axios";
import _ from "lodash";

export default {
  name: "book",
  data() {
    return {
      items: [],
      keyword: "",
      message: "",
    };
  },
  watch: {
    keyword: function () {
      this.message = "Please Wait...";
      this.debounceGetAnswer();
    },
  },
  created: function () {
    this.debounceGetAnswer = _.debounce(this.getAnswer, 1000);
  },
  methods: {
    getAnswer: function () {
      if (this.keyword === "") {
        this.items = null;
        this.message = "";
        return;
      }
      this.message = "Searching";
      var vm = this;
      var params = { page: 1, per_page: 10, query: this.keyword };
      console.log(params);
      axios
        .get(
          "https://www.googleapis.com/books/v1/volumes?q=search/" + params.query
        )
        .then(function (response) {
          vm.items = response.data.items;
        })
        .catch(function (error) {
          vm.message = "Error!" + error;
        })
        .finally(function () {
          vm.message = "";
        });
    },
  },
};
</script>

<style scoped>
.search-input {
  width: 300px;
  margin: 0 auto;
}
.card-title {
  font-size: 14px;
}
.card-text {
  font-size: 12px;
}
</style>
