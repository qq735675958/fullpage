<template>
  <div class="home">
    <h1>我是多页面配置的 - home</h1>
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
  mounted(){
    console.log(this.$store)
  }
};
</script>