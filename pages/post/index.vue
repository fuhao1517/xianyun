<template>
  <div>
    <div>旅游攻略首页</div>
    <h3>组件的递归</h3>
    <!-- 组件接收的是数组 -->
    <MenuItem :data="list" />
  </div>
</template>

<script>
import MenuItem from "@/components/post/menuItem";
export default {
  components: {
    MenuItem
  },
  data() {
    return {
      list: [
        {
          name: "服装",
          children: [
            {
              name: "男装",
              children: [
                { name: "正装" },
                { name: "休闲装" },
                { name: "运动装" }
              ]
            },
            {
              name: "女装",
              children: [
                { name: "正装" },
                { name: "休闲装" },
                { name: "运动装" },
                { name: "xxx" }
              ]
            },
            { name: "童装" }
          ]
        },
        {
          name: "电器",
          children: [{ name: "电视" }, { name: "空调" }, { name: "冰箱" }]
        }
      ]
    };
  }
};
</script>

<style>
</style>