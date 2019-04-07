<template>
<div>
  <div>
    <Rili></Rili>
  </div>
  <div class="hello">
    <mt-tabbar v-model="selected">
      <mt-tab-item id="工作">
        <img slot="icon" src="../assets/农产品.png">
        工作
      </mt-tab-item>
      <mt-tab-item id="角色">
        <img slot="icon" src="../assets/审核.png">
        角色
      </mt-tab-item>
      <mt-tab-item id="事项圈">
        <img slot="icon" src="../assets/等待.png">
        事项圈
      </mt-tab-item>
      <mt-tab-item id="同事">
        <img slot="icon" src="../assets/切换.png">
        同事
      </mt-tab-item>
      <mt-tab-item id="日历">
        <img slot="icon" src="../assets/我的土地.png">
        日历
      </mt-tab-item>
    </mt-tabbar>
  </div>
</div>
</template>

<script>
import Rili from './Rili'
export default {
  name: "FootGuide",
  components: {
    Rili
  },
  data () {
    return {
      selected: '日历'
    }
  },
  watch: {
    selected: function (val, oldVal) {
      console.log(val)
      // click后打印出当前mt-tab-item的id
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.mint-tabbar {
  position: fixed;
}
</style>
