<template>
  <div class="container">

    <div>
      <Calendar fixed class="cal" v-bind:class="{ 'cal-fold': isFold }" v-on:choseDay="clickDay" v-on:changeMonth="changeDate"></Calendar>
      <div class="drg">
        <i class="iconfont" v-bind:class="{ 'iconxiangxia': isFold, 'iconxiangshang': !isFold }" @click="up"></i>
      </div>
      <div class="cfm">
        <span>已设置提醒</span>
        <span>创建时间</span>
        <span>最后发言时间</span>
      </div>
    </div>

    <div class="ull">

        <div class="lii">
          <div class="title">227市场</div>
          <div class="content">定价依据和客户判定</div>
          <div class="role">我的角色：经办人</div>
        </div>

        <div class="lii">
          <div class="title">新软件</div>
          <div class="content">成立体验小组，测试软件</div>
          <div class="role">我的角色：交办人</div>
        </div>

        <div class="lii">
          <div class="title">2-3-6手提项目</div>
          <div class="content">236手提灭火器项目，10月需要提交给需求方</div>
          <div class="role">我的角色：交办人</div>
        </div>

    </div>

  </div>
</template>

<script>
import Calendar from "vue-calendar-component";
export default {
  components: {
    Calendar
  },
  data() {
    return {
      isFold: false
    };
  },
  methods: {
    clickDay(data) {
      console.log(data); //选中某天
    },
    changeDate(data) {
      console.log(data); //左右点击切换月份
    },
    clickToday(data) {
      console.log(data); //跳到了本月
    },
    up() {
      this.isFold = !this.isFold;
    }
  }
};
</script>

<style>
.wh_content_all[data-v-2ebcbc83]{
  background-color:white;
}
.wh_top_changge{
  background-color:lightskyblue;
}
.wh_content_item .wh_chose_day[data-v-2ebcbc83]{
  background-color: lightskyblue;
}
.drg {
  background-color:white;
  height: 20px;
  line-height: 20px;
  text-align: center;
}
.cfm {
  background-color:white;
  border-top: 1px rgba(0,0,0,0.1) solid;
  border-bottom: 1px rgba(0,0,0,0.1) solid;
  height: 40px;
  line-height: 40px;
  display: flex;
  justify-content: space-around;
}
span {
  font-size: 14px;
}
.lii {
  margin: 0;
  height: 90px;
  border-bottom: 1px rgba(0,0,0,0.1) solid;
}
.title{
color: black;
font-size: 18px;
margin-top: 8px;
margin-left: 20px;
}
.content{
color: darkgrey;
font-size: 14px;
margin-top: 6px;
margin-left: 20px;
}
.role{
color: lightskyblue;
font-size: 14px;
margin-top: 6px;
margin-left: 20px;
}
.cal-fold {
  height: 130px;
}
.cal {
  overflow: hidden;
  
}
.cal .wh_content_item {
color: black;
}
</style>
