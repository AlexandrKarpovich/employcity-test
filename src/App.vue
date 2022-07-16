<template>
  <div class="wrapper">
    <HeaderTop />
    <div class="main">
      <router-view/>
    </div>
    <FooterLine />
  </div>
</template>


<script>
import HeaderTop from './components/HeaderTop.vue'
import FooterLine from './components/FooterLine.vue'
export default {
  name: 'App',
  components: {
    HeaderTop,
    FooterLine
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

nav {
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
