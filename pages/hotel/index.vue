<template>
  <div style="padding:50px;">
    酒店模块首页
    <div id="container"></div>
  </div>
</template>

<script>
export default {
  mounted() {
    /* 整个页面加载完毕之后执行 */
    window.onLoad = function() {
      var map = new AMap.Map("container");
    };
    /* 地图的连接 */
    var url =
      "https://webapi.amap.com/maps?v=1.4.15&key=fd675b2c65d8924ae177ad3e95a75406&callback=onLoad";
    var jsapi = document.createElement("script");
    jsapi.charset = "utf-8";
    jsapi.src = url;
    document.head.appendChild(jsapi);
  }
};
</script>

<style scoped lang="less">
#container {
  width: 300px;
  height: 180px;
}
</style>