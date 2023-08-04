<template>
  <div id="app" :style="{ backgroundColor: currentColor }">
    <h1>Fun Color Party!</h1>
    <button @click="changeColor">Shuffle Color!</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      colors: ["red", "blue", "green", "yellow", "pink", "orange"],
      currentColor: "red",
    };
  },
  methods: {
    changeColor() {
      const index = Math.floor(Math.random() * this.colors.length);
      this.currentColor = this.colors[index];
    },
  },
  created() {
    this.changeColor();
  },
};
</script>

<style scoped>
#app {
  text-align: center;
  padding: 20px;
  height: 100vh;
  color: #fff;
}

button {
  padding: 10px 20px;
}
</style>