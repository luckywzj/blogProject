<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
import Main from "./components/mains/main";
export default {
    name: "App",
    data() {
        return {};
    },
    components: {
        Main
    }
};
</script>

<style>
body {
    background: url("../src/assets/imgs/menu_bg.png") repeat-x #efefef;
}
#app {
    font-family: "Avenir", Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    /* text-align: center; */
    color: #2c3e50;
    margin-top: 60px;
}
</style>
