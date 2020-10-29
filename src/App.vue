<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h1>{{ title.toUpperCase() }}</h1>
  <p v-html="magic"></p>
</template>


<script>
export default {
  data() {
    return {
      title: "First Vue 3 app!",
      magic: "<h1>lol</h1>"
    };
  }
};
</script>





<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
