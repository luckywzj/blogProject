<template>
  <div id="main">

    <logo></logo>`
    <navs></navs>
    <footers></footers>
  </div>
</template>
<script>
import Logo from "./logo";
import Navs from "./nav";
import Footers from "./footer";
export default {
    name: "Main",
    data() {
        return {};
    },
    components: {
        Logo,
        Navs,
        Footers
    }
};
</script>
<style scoped>
</style>
