<template>
  <div id="app">
    <div id="nav">
      <top-header></top-header>
    </div>
    <router-view />
    <bottom-footer></bottom-footer>
  </div>
</template>

<script>
import Header from "../src/components/Header";
import FooterVue from "./components/Footer.vue";

export default {
  components: {
    "top-header": Header,
    "bottom-footer": FooterVue
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
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
