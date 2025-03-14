<template>
  <h1>{{ title }}</h1>
  <Counter />
</template>

<script>
export default {
  name: 'App',
  data() {
    return { title: 'My First Vue app!' }
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ddd;
  margin-top: 60px;
}
body {
  background-color: #2c3e50;
}
h1 {
  border-bottom: 1px solid #ddd;
  padding-bottom: 10px;
  display: inline-block;
}
</style>
