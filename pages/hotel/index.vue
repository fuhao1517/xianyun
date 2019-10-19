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
      var map = new AMap.Map("container", {
        zoom: 11, //级别
        center: [113.3245904, 23.1066805] //中心点坐标
      });

      var marker = new AMap.Marker({
        content: `<div style="width:20px; height:20px; border-radius: 50px; background:red; color:#fff; text-align:center; line-height: 20px;">99</div>`,
        position: [113, 23.1066805] //位置
      });
      map.add(marker); //添加到地图
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
  width: 500px;
  height: 300px;
}
</style>