<template>
  <h1>{{ title }}</h1>
  <input type="text" ref="name" />
  <button @click="handleClick">Click me</button>
  <Counter />
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'My First Vue app!',
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name)
      this.$refs.name.classList.add('active')
      this.$refs.name.focus()
    },
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
