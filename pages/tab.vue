<template>
  <div class="btns">
    <span
      v-for="(item,index) in ['新闻','娱乐','体育']"
      :key="index"
      :class="{active:index===current}"
      @click="handleClick(index)"
    >{{item}}</span>

    <div v-if="current===0">
      <p>无锡上跨桥侧翻疑似涉事货车公司曝光:1年涉6起事故</p>
      <p>无锡上跨桥侧翻疑似涉事货车公司曝光:1年涉6起事故</p>
      <p>无锡上跨桥侧翻疑似涉事货车公司曝光:1年涉6起事故</p>
      <p>无锡上跨桥侧翻疑似涉事货车公司曝光:1年涉6起事故</p>
    </div>

    <div v-if="current===1">
      <p>明星外卖名搞笑：热巴叫老王大张伟叫梁朝伟</p>
      <p>明星外卖名搞笑：热巴叫老王大张伟叫梁朝伟</p>
      <p>明星外卖名搞笑：热巴叫老王大张伟叫梁朝伟</p>
      <p>明星外卖名搞笑：热巴叫老王大张伟叫梁朝伟</p>
    </div>

    <div v-if="current===2">
      <p>全民皆兵！活塞全队7人得分上双力克独行侠</p>
      <p>全民皆兵！活塞全队7人得分上双力克独行侠</p>
      <p>全民皆兵！活塞全队7人得分上双力克独行侠</p>
      <p>全民皆兵！活塞全队7人得分上双力克独行侠</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      current: 0
    };
  },
  methods: {
    handleClick(index) {
      this.current = index;
    }
  }
};
</script>

<style scoped lang="less">
.btns {
  padding: 50px;
  span {
    border: 1px solid #eee;
    padding: 5px;
  }
  div {
    margin-top: 50px;
  }
  .active {
    background: red;
  }
}
</style>