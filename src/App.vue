<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
      <router-link to="/signup">Signup</router-link>
    </div>
    <router-view class="main-content"/>
  </div>
</template>

<style lang="scss">
html, body {
  margin: 0;
  padding: 0;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
}
#nav {
  position: absolute;
  top: 10px;
  bottom: 10px;
  width: 300px;
  padding: 50px 30px;
  margin: 10px 0;
  box-sizing: border-box;
  border-right: 1px solid #ccc;
  a {
    display: block;
    margin-bottom: 10px;
    font-weight: bold;
    color: #2c3e50;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}

.main-content {
  margin-left: 300px;
  padding: 50px 100px;
}
</style>
