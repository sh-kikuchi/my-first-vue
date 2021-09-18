<template>
  <div id="color">
    <h1 class="page-title">Find your color</h1>
    <h3 class="page-sub-title">あなただけのお気に入りの色を探してみましょう</h3>
    <div :style="bindStyle" class="circle"></div>
    <div class="contents color-content">
      <div>
        <span>R:</span>
        <input v-model="red" type="range" max="255" min="0" />
      </div>
      <div>
        <span>G:</span>
        <input v-model="green" type="range" max="255" min="0" />
      </div>
      <div>
        <span>B:</span>
        <input v-model="blue" type="range" max="255" min="0" />
      </div>
      <div>
        <span>a:</span>
        <input v-model="opacity" type="range" max="1" min="0" step="0.1" />
      </div>
      <div>
        color: rgba({{ red }},{{ green }},{{ blue }},{{ opacity }})<br />
        background-color: rgba({{ red }},{{ green }},{{ blue }},{{ opacity }})
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      red: 0,
      blue: 0,
      green: 0,
      opacity: 1,
    };
  },
  computed: {
    bindStyle() {
      return `background-color: rgba(${this.red},${this.green},${this.blue},${this.opacity})`;
    },
  },
};
</script>
<style scoped>
.circle {
  width: 200px;
  height: 200px;
  background-color: grey;
  margin: 0 auto;
  border-radius: 50%;
}

.color-content {
  width: 400px;
  text-align: center;
}
</style>
