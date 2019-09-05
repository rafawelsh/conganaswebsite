<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link> |
      <router-link to="/lookbook">Lookbook</router-link> |
      <router-link to="/contact">Contact</router-link> |
    </div>
    <router-view />
  </div>
</template>

<style lang="scss">
#app {
  
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  background: rgba(40, 39, 40);
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  padding: 20px;
  a {
    font-weight: bold;
    color: #cbcfd3;
    &.router-link-exact-active {
      color: #42b983;
    }
    &:hover {
      color: #42b983;
    }
  }
}
</style>
