<template>
  <div id="app">
    <div id="nav">
      <img src="./assets/images/HouseA_logo.png"><br>
      <router-link to="/">Home</router-link> |
      <router-link to="/recipes">Recipes</router-link> |
      <router-link to="/catalog">Catalog</router-link>
    </div>
    <router-view />
    <footer id="footer">Website by House Atreides 2020</footer>
  </div>
</template>

<style lang="scss">
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
