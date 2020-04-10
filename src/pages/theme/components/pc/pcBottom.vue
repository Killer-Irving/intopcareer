<template>
  <div class="pc-bottom">
    <div class="part1">
      <div class="content">
        <div class="left">
          <img src="@/assets/imgs/bottom_logo.png" class="logo-img" />
          <span class="text1">北京总部：北京市海淀区中关村软件园立思辰大厦</span>
          <span class="text1">广州中心：广州市越秀区先烈中路东山广场1019-20室</span>
          <span class="text1">大连中心：大连市沙河口区西安路天兴罗斯福国际大厦</span>
        </div>
        <div class="right">
          <div class="item">
            <img src="@/assets/imgs/service.png" class="code-img" />
            <span class="text2">盈途教育服务号</span>
          </div>
          <div class="item">
            <img src="@/assets/imgs/subscribe.png" class="code-img" />
            <span class="text2">盈途教育订阅号</span>
          </div>
        </div>
      </div>
    </div>

    <div class="part2">
      <span class="text1">Copyright © 2007-2019 inTopCareer.COM All Rights Reserved 盈途教育 版权所有</span>
      <span class="text1">京ICP备19001718号 京公网安备1101082083</span>
    </div>
  </div>
</template>


<script>
export default {
  name: "pcHeader",
  data() {
    return {};
  },
  props: {},
  components: {},
  mounted() {},
  created() {},
  computed: {},
  watch: {},
  methods: {}
};
</script>
<style lang="scss" scoped>
.pc-bottom {
  height: 274px;
}
.part1 {
  height: 200px;
  background: rgba(81, 81, 81, 1);
  display: flex;
  align-items: center;
  justify-content: center;
  .content {
    display: flex;
    justify-content: space-between;
    height: 200px;
    width: 1180px;
    .left {
      display: flex;
      flex-direction: column;
      .logo-img {
        width: 215px;
        height: 54px;
        margin-top: 36px;
        margin-bottom: 14px;
      }
      .text1 {
        font-size: 14px;
        font-family: PingFangSC-Regular, PingFang SC;
        font-weight: 400;
        color: rgba(176, 176, 176, 1);
        line-height: 24px;
      }
    }
    .right {
      display: flex;
      .item {
        display: flex;
        flex-direction: column;
        margin-left: 30px;
        .code-img {
          width: 100px;
          height: 100px;
          margin-top: 40px;
          margin-bottom: 5px;
        }
        .text2 {
          font-size: 14px;
          font-family: PingFangSC-Regular, PingFang SC;
          font-weight: 400;
          color: #b0b0b0;
        }
      }
    }
  }
}
.part2 {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: rgba(52, 52, 52, 1);
  height: 74px;
  .text1 {
    font-size: 14px;
    font-family: PingFangSC-Regular, PingFang SC;
    font-weight: 400;
    color: rgba(153, 153, 153, 1);
    line-height: 22px;
  }
}
</style>