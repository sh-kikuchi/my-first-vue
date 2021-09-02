<template>
  <div id="color">
    <div :style="bindStyle" class="square"></div>
    <div>
      <span>R:</span>
      <input v-model="red" type="range" max="255" min="0" />
      {{ red }}
    </div>
    <div>
      <span>G:</span>
      <input v-model="green" type="range" max="255" min="0" />
      {{ green }}
    </div>
    <div>
      <span>B:</span>
      <input v-model="blue" type="range" max="255" min="0" />
      {{ blue }}
    </div>
    <div>background-color: rgb({{ red }},{{ green }},{{ blue }})</div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      red: 0,
      blue: 0,
      green: 0,
    };
  },
  computed: {
    bindStyle() {
      return `background: rgb(${this.red},${this.green},${this.blue})`;
    },
  },
};
</script>
<style scoped>
.square {
  width: 100px;
  height: 100px;
  background-color: grey;
  margin: 0 auto;
}
</style>
