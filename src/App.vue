<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <Navbar></Navbar>
    <div class="body_part">
      <Sidebar></Sidebar>
      <home></home>

    </div>
    <Foote></Foote>
    <Menu></Menu>
    <router-view/>
  </div>
</template>
<script>
import home from './views/pages/Home'
import Navbar from './views/layout/Navbar'
import Sidebar from './views/layout/Sidebar'
import Foote from './views/layout/Foote'
import Menu from './views/layout/Menu'




export default {
  name: 'App',
  components: {
    Sidebar,
    Navbar,
    home,
    Foote,
    Menu,
  }
}
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
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
