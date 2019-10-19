<template>
  <div>
    酒店模块首页
    <!-- <script
      type="text/javascript"
      src="https://webapi.amap.com/maps?v=1.4.15&key=fd675b2c65d8924ae177ad3e95a75406"
    ></script>-->
    <script type="text/javascript" src="https://webapi.amap.com/maps?v=1.4.15&key=fd675b2c65d8924ae177ad3e95a75406"></script>
    <div id="container"></div>
  </div>
</template>

<script>
export default {
  mounted() {
    window.onLoad = function() {
      var map = new AMap.Map("container");
    };
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