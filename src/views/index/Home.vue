<template>
  <div class="home">
    我是 index - home 页
    <HelloWorld msg="hello 小红 我配好了" />
    
    <a href='page2.html'>点击我就能跳过去😯  前往page2页面</a>

    <div class="mar-50">
      <el-carousel indicator-position="outside">
    <el-carousel-item v-for="item in 4" :key="item">
      <h3>{{ item }}</h3>
    </el-carousel-item>
  </el-carousel>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "./components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld
  },
  beforeDestroy(){
    console.log(888)
  },
  data(){
    return {
      imgarr:[
        {src:''},
        {},
        {},
      ]
    }
  }
};
</script>
<style lang="less">
  .mar-50{
    margin-top: 50px;
  }

   .el-carousel__item h3 {
    color: #475669;
    font-size: 18px;
    opacity: 0.75;
    line-height: 300px;
    margin: 0;
  }
  
  .el-carousel__item:nth-child(2n) {
    background-color: #99a9bf;
  }
  
  .el-carousel__item:nth-child(2n+1) {
    background-color: #d3dce6;
  }
</style>