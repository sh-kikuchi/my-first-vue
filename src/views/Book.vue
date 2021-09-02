<template>
  <div id="book">
    <h1>Books</h1>
    <p>
      <input type="text" v-model="keyword" />
    </p>
    <div>
      {{ message }}
    </div>
    <div class="book_card" v-for="(item, index) in items" :key="index">
      <div class="card-body">
        <p class="card-title">{{ item.volumeInfo.title }}</p>
        <p class="card-text">{{ item.volumeInfo.authors }}</p>
        <p class="card-text">{{ item.volumeInfo.publisher }}</p>
      </div>
    </div>
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
</style>
