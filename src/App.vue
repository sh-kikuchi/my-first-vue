<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">@HOME</router-link>
      <router-link to="/work">WorkS</router-link>
      <router-link to="/list">ListS</router-link>
      <router-link to="/color">ColorS</router-link>
      <router-link to="/book">BookS</router-link>
    </div>
    <router-view />
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 20px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding-right: 10px;
  padding-left: 10px;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
