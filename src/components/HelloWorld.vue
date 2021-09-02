<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="square">
      <div class="sub-square" v-for="(content, index) in contents" :key="index">
        <h3>{{ content.title }}</h3>
        <p>{{ content.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  data() {
    return {
      contents: [
        {
          title: "VIEWS",
          text: "【vue-slick-carousel】を使用した写真スライド。",
        },
        {
          title: "LISTS",
          text: "『太陽のパスタ、豆のスープ』よりドリフターズリスト！",
        },
        {
          title: "COLORS",
          text: "三原色からあなただけの色を探そう",
        },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.square {
  display: flex;
  justify-content: space-around;
  flex-wrap: nowrap;
}
.sub-square {
  width: 300px;
  height: 300px;
}
.sub-square:nth-child(even) {
  border: 1px solid #000000;
}
.sub-square:nth-child(odd) {
  background-color: rgba(66, 185, 131, 0.5);
}
</style>
