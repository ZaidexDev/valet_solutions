<template>
  <navbar-global />
  <router-view/>
</template>


<script>
import NavbarGlobal from './components/NavbarGlobal.vue';

export default {
  components: { NavbarGlobal },
  data() {
    return {

    }
  }
}
</script>

<style lang="scss">
@import './assets/style/style.css';
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

#nav {
  

  a {
    
    

    &.router-link-exact-active {
      
      
    }
  }
}
</style>
