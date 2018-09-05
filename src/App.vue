<template>
  <div id="app" class=" container ">
    <nav id="nav" class="navbar navbar-dark bg-dark justify-content-center">
      <li class="nav-item">
        <router-link class="nav-link" to="/">Store</router-link>
      </li>
      <li class="nav-item">
        <router-link class="nav-link" to="/about">About</router-link>
      </li>
    </nav>
    <router-view/>
  </div>
</template>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
  a {
    font-weight: bold;
    color: #ecf0f3;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
