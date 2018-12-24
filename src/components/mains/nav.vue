<template>
  <div id="nav">
    <el-tabs :tab-position="tabPosition" style="min-height:480px">
      <el-tab-pane label="首页">
        <home></home>
      </el-tab-pane>
      <el-tab-pane label="我的日记">
        <Photo></Photo>
      </el-tab-pane>
      <el-tab-pane label="关于我">角色管理</el-tab-pane>
      <el-tab-pane label="内容页">定时任务补偿</el-tab-pane>
    </el-tabs>
  </div>
</template>
<script>
import Home from "./home";
import Photo from './photo';

export default {
    data() {
        return {
            tabPosition: "top",

        };
    },
    components: {
        Home,
        Photo
    },
    mounted() {

    },
    methods: {

    }
};
</script>
<style scoped>
#nav {
    width: 80%;
    margin: 0 auto;
}
</style>
