<template>
  <div id="list">
    <h1>This is a Drifter's list page</h1>
    <input type="card" v-model="card" />
    <button @click="addCard">追加する</button>
    <draggable v-model="lists" @end="onEnd">
      <div class="card" v-for="(list, index) in lists" :key="index">
        <div class="list-index">{{ index + 1 }}</div>
        <div class="list-text">{{ list }}</div>
        <div>
          <button class="btn btn-danger" @click="removeCard(index)">✖</button>
        </div>
      </div>
    </draggable>
  </div>
</template>
<script>
import draggable from "vuedraggable";
export default {
  components: {
    draggable,
  },
  data() {
    return {
      lists: ["映画を見ること", "美術館に行く", "美味しいものを食べる"],
      card: null,
    };
  },
  mounted() {
    //mounted は値を取得し JSON の値を解析する
    if (localStorage.getItem("lists")) {
      try {
        this.lists = JSON.parse(localStorage.getItem("lists"));
      } catch (e) {
        localStorage.removeItem("lists");
      }
    }
  },
  methods: {
    addCard() {
      //もし未入力の場合
      if (!this.card) {
        return;
      }
      //カードをリストに追加
      this.lists.push(this.card);
      this.card = "";
      //データ保存
      this.saveLists();
    },
    removeCard(index) {
      //カード削除
      this.lists.splice(index, 1);
      //データ保存
      this.saveLists();
    },
    saveLists() {
      //JSONに格納するために文字列化
      const parsed = JSON.stringify(this.lists);
      //配列をJSON形式の文字列にして保存する
      localStorage.setItem("lists", parsed);
      console.log(localStorage);
    },
    //並べ替えの時にデータを保存
    onEnd() {
      window.localStorage.setItem("lists", JSON.stringify(this.lists));
    },
    created() {
      if (window.localStorage.getItem("lists")) {
        this.lists = JSON.parse(localStorage.getItem("lists"));
      }
    },
  },
};
</script>
<style scoped>
.card {
  display: flex;
  justify-content: center;
  flex-wrap: nowrap;
}
.list-text {
  width: 400px;
}
</style>>
