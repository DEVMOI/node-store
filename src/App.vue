<template>
  <div id="app" class=" container-fluid p-0">
    <nav id="nav" class="navbar navbar-dark bg-black justify-content-start">
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
  list-style: none;
  padding: 15px 0;
  a {
    font-weight: bold;
    color: #ecf0f3;
    &.router-link-exact-active {
      color: #cf6dca;
    }
  }
}
.bg-black{
  background-color: #000;
}
</style>
