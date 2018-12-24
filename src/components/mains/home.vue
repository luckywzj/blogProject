<template>
  <div id="home">
    <div class="left">

      <ul>
         <h5>about me</h5>
        <i><img
            src="../../assets/imgs/4.jpg"
            alt=""
          ></i>
        <p>
          <b>三木</b>
          ，前端程序员，16年从事安卓开发，17年开始从事前端开发。。
        </p>
      </ul>
      <Timer></Timer>
    </div>
    <div class="right">
      <div v-for="item in artleList">
        <router-link tag="li":to="{name:'Content',query:{id:item.id}}">
          <h3>{{item.title}}</h3>
          <p>{{item.content}}</p>
          <p>{{item.updateTime}}</p>

        </router-link>

        <i><img v-bind:src="item.photosrc" alt=""></i>
      </div>
    </div>
  </div>
</template>
<script>
import Timer from "./timer";
export default {
  data() {
    return {
      artleList: [
        {
          title: "",
          photosrc: "",
          content: ""
        }
      ]
    };
  },
  components:{
    Timer
  },
  mounted() {
    this.getGoodsList();
  },
  methods: {
    getGoodsList() {
      this.$http.get("../../../static/falsedata.json").then(res => {
        var result = res.data;
        console.log(result);
        this.artleList = result.artle;
      });
    }
  }
};
</script><style scoped>
#home {
  display: flex;
  justify-content: space-between;
}
a {
  text-decoration: none;
}
.router-link-active {
  text-decoration: none;
}
ul {
  padding: 10px;
  background: #fff;
}
.right div {
  list-style: none;
  background: rgba(255, 255, 255, 1);
  padding-left: 15px;
  overflow: hidden;
  color: #797b7c;
  font-size: 1em;
  margin-bottom: 15px;
  display: flex;
}
.left {
  width: 25%;
  height: 100%;
  text-align: center;
}

.left i {
  width: 120px;
  float: left;
  clear: left;
  margin-right: 10px;
  height: 80px;
  overflow: hidden;
}
.left img {
  width: 100%;
  border-radius: 50%;
}
.left p {
  line-height: 24px;
  font-size: 14px;
}
.right {
  width: 70%;
}
.right div{
  border-radius: 4px;
 box-shadow:0px 5px 10px rgba(0,0,0,.4);
}
.right div img {
  width: 150px;
  padding: 10px;
}
</style>
