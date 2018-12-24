<template>
  <div id="test">

    <div class="contentAll"  >
      <h3>  {{artleDatas.title}}</h3>
      <div class="contentMain">
        <p v-html = 'artleDatas.content'> </p>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "contents",
  data() {
    return {
      artleDatas:
        {
          title: "",
          content: ""
        }

    };
  },
  created() {},
  mounted() {
    this.getArtlesContent();
  },
  methods: {
    getArtlesContent() {
      this.$http.get("../../../static/artledata.json").then(res => {
        let result = res.data;
        let data = result.data;
        data.forEach(element => {

          if (element.id == this.$route.query.id) {
            this.artleDatas = element;
          }
        });
      });
    }
  }
};
</script>
<style lang="less" scoped>
.contentAll {
  width: 70%;
  margin: 0 auto;
  background-color: #eff;
  .el-icon-back {
    padding: 20px;
    color: #409eff;
  }
  h3 {
    line-height: 50px;
    text-align: center;
    
  }
  .contentMain {
    min-height: 500px;
    width: 80%;
    margin: 0 auto;
    font-size: 1em;
    p {
     line-height:30px
    }
  }
}
</style>
