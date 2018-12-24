<template>
  <div class="footers">
    <p>{{msg}}</p>
  </div>
</template>
<script>
export default {
    name: "Footers",
    data() {
        return {
            msg: "Design by 三木个人博客   豫ICP备18008075号-1"
        };
    }
};
</script>
<style scoped>
.footers {
    text-align: center;
    font-size:13px
}
</style>
