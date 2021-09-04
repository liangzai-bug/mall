<template>
  <div id="app">
    <div id="nav">
      <h1>{{ $store.state.count }}</h1>
      <button @click="add1()">+</button>
      <button @click="stu1()">-</button>
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
export default {
  methods: {
    add1() {
      this.$store.commit("add");
    },
    stu1() {
      this.$store.commit("stu");
    },
  },
};
</script>

<style lang="less">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
