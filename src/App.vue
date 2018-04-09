<template>
  <div id="app">
    <h1>My Todo App!</h1>
    <router-view/>
    <footer>Created by Yao(https://github.com/datouyu123)</footer>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style lang="scss">

*, *::before, *::after {
  box-sizing: border-box;
}

#app {
  max-width: 400px;
  min-height:100%;
  margin: 0 auto;
  line-height: 1.4;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #32485F;
}

footer {
  margin:60px 0 30px 0;
}

h1 {
  text-align: center;
}
</style>
